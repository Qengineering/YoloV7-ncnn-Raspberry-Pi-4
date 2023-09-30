# YoloV7 Raspberry Pi 4
![output image]( https://qengineering.eu/images/ParkingYoloV7.jpg )
## YoloV7 with the ncnn framework. <br/>
[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)<br/><br/>
Paper: https://arxiv.org/pdf/2207.02696.pdf<br/><br/>
Special made for a bare Raspberry Pi 4, see [Q-engineering deep learning examples](https://qengineering.eu/deep-learning-examples-on-raspberry-32-64-os.html)

------------

## Benchmark.
| Model  | size | mAP | Jetson Nano | RPi 4 1950 | RPi 5 2900 | Rock 5 | 
| ------------- | :-----:  | :-----:  | :-------------:  | :-------------: | :-----: | :-----: |
| [NanoDet](https://github.com/Qengineering/NanoDet-ncnn-Raspberry-Pi-4) | 320x320 | 20.6  |  26.2 FPS | 13.0 FPS | 43.2 FPS |36.0 FPS |
| [NanoDet Plus](https://github.com/Qengineering/NanoDetPlus-ncnn-Raspberry-Pi-4) | 416x416 | 30.4  |  18.5 FPS | 5.0 FPS | 30.0 FPS | 24.9 FPS |
| [PP-PicoDet](https://github.com/Qengineering/PP-PicoDet-ncnn-Raspberry-Pi-4) | 320x320 | 27.0  |  24.0 FPS | 7.5 FPS | 53.7 FPS | 46.7 FPS |
| [YoloFastestV2](https://github.com/Qengineering/YoloFastestV2-ncnn-Raspberry-Pi-4) | 352x352 | 24.1 |  38.4 FPS | 18.8 FPS | 78.5 FPS | 65.4 FPS | 
| [YoloV2](https://github.com/Qengineering/YoloV2-ncnn-Raspberry-Pi-4) <sup>20</sup>| 416x416 | 19.2 |  10.1 FPS | 3.0 FPS | 24.0 FPS | 20.0 FPS | 
| [YoloV3](https://github.com/Qengineering/YoloV3-ncnn-Raspberry-Pi-4) <sup>20</sup>| 352x352 tiny | 16.6 | 17.7 FPS | 4.4 FPS | 18.1 FPS | 15.0 FPS | 
| [YoloV4](https://github.com/Qengineering/YoloV4-ncnn-Raspberry-Pi-4) | 416x416 tiny | 21.7 | 16.1 FPS | 3.4 FPS | 26.8 FPS | 22.4 FPS | 
| [YoloV4](https://github.com/Qengineering/YoloV4-ncnn-Raspberry-Pi-4) | 608x608 full | 45.3 | 1.3 FPS | 0.2 FPS | 1.82 FPS | 1.5 FPS | 
| [YoloV5](https://github.com/Qengineering/YoloV5-ncnn-Raspberry-Pi-4) | 640x640 small | 22.5 | 5.0 FPS | 1.6 FPS | 14.9 FPS | 12.5 FPS | 
| [YoloV6](https://github.com/Qengineering/YoloV6-ncnn-Raspberry-Pi-4) | 640x640 nano | 35.0 | 10.5 FPS | 2.7 FPS | 25.0 FPS | 20.8 FPS | 
| [YoloV7](https://github.com/Qengineering/YoloV5-ncnn-Raspberry-Pi-4) | 640x640 tiny | 38.7 | 8.5 FPS | 2.1 FPS | 21.5 FPS | 17.9 FPS | 
| [YoloV8](https://github.com/Qengineering/YoloV8-ncnn-Raspberry-Pi-4) | 640x640 nano | 37.3 | 14.5 FPS | 3.1 FPS | 20.0 FPS | 16.3 FPS | 
| [YoloV8](https://github.com/Qengineering/YoloV8-ncnn-Raspberry-Pi-4) | 640x640 small | 44.9 | 4.5 FPS | 1.47 FPS | 11.0 FPS | 9.2 FPS | 
| [YoloX](https://github.com/Qengineering/YoloX-ncnn-Raspberry-Pi-4) | 416x416 nano | 25.8 | 22.6 FPS | 7.0 FPS | 34.2 FPS | 28.5 FPS | 
| [YoloX](https://github.com/Qengineering/YoloX-ncnn-Raspberry-Pi-4) | 416x416 tiny | 32.8 | 11.35 FPS | 2.8 FPS | 21.8 FPS | 18.1 FPS | 
| [YoloX](https://github.com/Qengineering/YoloX-ncnn-Raspberry-Pi-4) | 640x640 small | 40.5 | 3.65 FPS | 0.9 FPS | 9.0 FPS | 7.5 FPS | 

<b><sup>20</sup></b> Recognize 20 objects (VOC) instead of 80 (COCO)

------------

## Dependencies.
To run the application, you have to:
- A Raspberry Pi 4 with a 32 or 64-bit operating system. It can be the Raspberry 64-bit OS, or Ubuntu 18.04 / 20.04. [Install 64-bit OS](https://qengineering.eu/install-raspberry-64-os.html) <br/>
- The Tencent ncnn framework installed. [Install ncnn](https://qengineering.eu/install-ncnn-on-raspberry-pi-4.html) <br/>
- OpenCV 64-bit installed. [Install OpenCV 4.5](https://qengineering.eu/install-opencv-4.5-on-raspberry-64-os.html) <br/>
- Code::Blocks installed. (```$ sudo apt-get install codeblocks```)

------------

## Installing the app.
To extract and run the network in Code::Blocks <br/>
$ mkdir *MyDir* <br/>
$ cd *MyDir* <br/>
$ wget https://github.com/Qengineering/YoloV7-ncnn-Raspberry-Pi-4/archive/refs/heads/main.zip <br/>
$ unzip -j master.zip <br/>
Remove master.zip, LICENSE and README.md as they are no longer needed. <br/> 
$ rm master.zip <br/>
$ rm LICENSE <br/>
$ rm README.md <br/> <br/>
Your *MyDir* folder must now look like this: <br/> 
parking.jpg <br/>
busstop.jpg <br/>
YoloV7.cpb <br/>
yolo.cpp <br/>
yolo.h <br/>
yoloV7main.cpp <br/>
yolov7-tiny.bin <br/>
yolov7-tiny.param <br/>

------------

## Running the app.
To run the application load the project file YoloV7.cbp in Code::Blocks. More info or<br/> 
if you want to connect a camera to the app, follow the instructions at [Hands-On](https://qengineering.eu/deep-learning-examples-on-raspberry-32-64-os.html#HandsOn).<br/><br/>

------------

### Dynamic sizes.
YoloV7 can handle different input resolutions without changing the deep learning model.<br/>
On line 28 of `yolov7main.cpp` you can change the `target_size` (default 640).<br/>
Decreasing the size to say 412 will speed up the inference time. On the other hand, the resizing makes the image less detailed; the model will no longer detect all objects.<br/><br/>

Many thanks to [nihui](https://github.com/nihui/) and [Xiang Shin Wuu](https://github.com/xiang-wuu)<br/><br/>
![output image]( https://qengineering.eu/images/BusstopYoloV7.jpg )

------------

[![paypal](https://qengineering.eu/images/TipJarSmall4.png)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=CPZTM5BB3FCYL) 


