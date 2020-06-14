# YOLOv3v4-Docker
Compile YOLO from [AlexeyAB/darknet](https://github.com/AlexeyAB/darknet#requirements) as C++ DLL-file on Windows and Build a Linux-CUDA-Docker to use SO-file.
## 1. Run darknet.exe directly on Windows 10 (CUDA 10.1+OpenCV 4.3.0)
1. download darknet from [Google Drive](https://drive.google.com/file/d/1nsjulqleP953mkWo5GCqHdXbM7aS-tgl/view?usp=sharing) (if you have same CUDA and OpenCV, you may run it successfully);
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

If you have installed different versions of CUDA and OpenCV, I recommend you to compile your darknet.exe as described in [blog](https://www.jianshu.com/p/f944ebd43f4c).
## 2. Compile yolo_cpp_dll.dll and generate yolo_cpp_dll.lib 
Reference: http://yy-programer.blogspot.com/2019/01/yolo-darknet.html (step-by-step tutorial in Chinese)
## 3. Use yolo_cpp_dll.dll in your C++ console application and python example
1. enter darknet\build\darknet\x64\ folder;
2. (C++) yolo_console_dll.exe
3. (Python) python darknet.py
## 4. Build a Linux-CUDA-Docker image
xxx
## References
1. [YOLOv4: Optimal Speed and Accuracy of Object Detection. arXiv 2004.10934.](https://arxiv.org/abs/2004.10934)
2. [YOLOv3: An Incremental Improvement. arXiv 1804.02767.](https://arxiv.org/abs/1804.02767)
