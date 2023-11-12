The method to install Yolo4 darknet
------
git clone https://github.com/AlexeyAB/darknet  

Train the model
------
cd C:\Users\az567\darknet1  

darknet.exe detector train Fire_detection/cfg/fire.data Fire_detection/cfg/yolov4-fire.cfg Fire_detection/cfg/yolov4-fire_best.weights -map  

Original weights: yolov4.conv.137  
After training , weights: yolov4-fire_best.weights  

Test the model
------

darknet.exe detector test Fire_detection/cfg/fire.data Fire_detection/cfg/yolov4-fire.cfg Fire_detection/cfg/weights/yolov4-fire_best.weights  C:/yolov7/yolov7dataset0/test/JPEGImages/10.jpg   

Calculate the mAP
------

darknet.exe detector map Fire_detection/cfg/fire.data Fire_detection/cfg/yolov4-fire.cfg Fire_detection/cfg/weights/yolov4-fire_best.weights  

