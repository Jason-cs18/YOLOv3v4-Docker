# YOLOv3v4-Docker
Compile YOLO as C++ DLL-file and Build a Linux-GPU-Docker to use this .dll
# Run darknet.exe directly on Windows 10 (CUDA 10.1+OpenCV 4.3.0)
1. download darknet from (if you have same CUDA and OpenCV, you may run it successfully);
2. extract darknet folder from darknet.7z;
3. enter darknet folder (you can see darknet.exe in this folder);
4. download yolov4.weights (245MB) to darknet folder: wget -c https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.weights;
5. download yolov3.weights (236MB) to darknet folder: wget -c https://pjreddie.com/media/files/yolov3.weights;
6. Run darknet.exe with YOLOv3: darknet.exe detect cfg\yolov3.cfg yolov3.weights data\dog.jpg
7. Run darknet.exe with YOLOv4: darknet.exe detect cfg\yolov4.cfg yolov4.weights data\dog.jpg </br>

**System variables on my PC:** 
1. CUDA_PATH: C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.1
2. CUDA_PATH_V10_1: C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.1
3. CUDNN: C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.1\bin
4. OpenCV_DIR: D:\Software\opencv\build
5. PATH: C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.1\libnvvp; D:\Software\opencv\build\x64\vc15\bin; D:\Software\opencv\build\x64\vc15\lib; D:\Code\darknet\build\darknet\x64

If you install different versions of CUDA and OpenCV, I recommend you to compile your darknet.exe as described in [blog]https://www.jianshu.com/p/f944ebd43f4c
