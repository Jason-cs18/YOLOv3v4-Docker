# YOLOv3v4-Docker
Compile YOLO as C++ DLL-file and Build a Linux-GPU-Docker to use this .dll
# Run darknet.exe directly on Windows 10
1. download darknet from ;
2. extract darknet folder from darknet.7z;
3. enter darknet folder (you can see darknet.exe in this folder);
4. download yolov4.weights (245MB) to darknet folder: wget -c https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.weights;
5. download yolov3.weights (236MB) to darknet folder: wget -c https://pjreddie.com/media/files/yolov3.weights;
6. Run darknet.exe with YOLOv3: darknet.exe detect cfg\yolov3.cfg yolov3.weights data\dog.jpg
7. Run darknet.exe with YOLOv4: darknet.exe detect cfg\yolov4.cfg yolov4.weights data\dog.jpg </br>

Note: 
1. xxx
2. xxx
