# YoloV5 Raspberry Pi 4
![output image]( https://qengineering.eu/images/test_parkV5.jpg )
## YoloV5 with the ncnn framework. <br/>
[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)<br/><br/>
Paper: https://towardsdatascience.com/yolo-v5-is-here-b668ce2a4908<br/><br/>
Specially made for a bare Raspberry Pi 4, see [Q-engineering deep learning examples](https://qengineering.eu/deep-learning-examples-on-raspberry-32-64-os.html)

------------

## Benchmark.
Numbers in **FPS** and reflect only the inference timing. Grabbing frames, post-processing and drawing are not taken into account.

| Model  | size | mAP | Jetson Nano | RPi 4 1950 | RPi 5 2900 | Rock 5 | RK3588<br>NPU | RK3566/68<br>NPU | Nano<br>TensorRT | Orin<br>TensorRT |
| ------------- | :-----:  | :-----:  | :-------------:  | :-------------: | :-----: | :-----: | :-------------:  | :-------------: | :-----: | :-----: |
| [NanoDet](https://github.com/Qengineering/NanoDet-ncnn-Raspberry-Pi-4) | 320x320 | 20.6  |  26.2 | 13.0 | 43.2  |36.0  |||||
| [NanoDet Plus](https://github.com/Qengineering/NanoDetPlus-ncnn-Raspberry-Pi-4) | 416x416 | 30.4  |  18.5  | 5.0  | 30.0  | 24.9  |||||
| [PP-PicoDet](https://github.com/Qengineering/PP-PicoDet-ncnn-Raspberry-Pi-4) | 320x320 | 27.0  |  24.0 | 7.5 | 53.7 | 46.7 |||||
| [YoloFastestV2](https://github.com/Qengineering/YoloFastestV2-ncnn-Raspberry-Pi-4) | 352x352 | 24.1 |  38.4 | 18.8 | 78.5 | 65.4 | ||||
| [YoloV2](https://github.com/Qengineering/YoloV2-ncnn-Raspberry-Pi-4) <sup>20</sup>| 416x416 | 19.2 |  10.1 | 3.0 | 24.0 | 20.0 | ||||
| [YoloV3](https://github.com/Qengineering/YoloV3-ncnn-Raspberry-Pi-4) <sup>20</sup>| 352x352 tiny | 16.6 | 17.7 | 4.4 | 18.1 | 15.0 | ||||
| [YoloV4](https://github.com/Qengineering/YoloV4-ncnn-Raspberry-Pi-4) | 416x416 tiny | 21.7 | 16.1 | 3.4 | 26.8 | 22.4 | ||||
| [YoloV4](https://github.com/Qengineering/YoloV4-ncnn-Raspberry-Pi-4) | 608x608 full | 45.3 | 1.3 | 0.2 | 1.82 | 1.5 | ||||
| [YoloV5](https://github.com/Qengineering/YoloV5-ncnn-Raspberry-Pi-4) | 640x640 nano | 22.5 | 5.0 | 1.6 | 14.9 | 12.5 | 58.8 | 14.8 | 19.0 | 100 |
| [YoloV5](https://github.com/Qengineering/YoloV5-ncnn-Raspberry-Pi-4) | 640x640 small | 22.5 | 5.0 | 1.6 | 14.9 | 12.5 | 37.7 | 11.7 | 9.25 | 100 |
| [YoloV6](https://github.com/Qengineering/YoloV6-ncnn-Raspberry-Pi-4) | 640x640 nano | 35.0 | 10.5 | 2.7 | 25.0 | 20.8 | 63.0 | 18.0 |||
| [YoloV7](https://github.com/Qengineering/YoloV5-ncnn-Raspberry-Pi-4) | 640x640 tiny | 38.7 | 8.5 | 2.1 | 21.5 | 17.9 |  53.4 | 16.1 | 15.0 ||
| [YoloV8](https://github.com/Qengineering/YoloV8-ncnn-Raspberry-Pi-4) | 640x640 nano | 37.3 | 14.5 | 3.1 | 20.0 | 16.3 | 53.1 | 18.2 |||
| [YoloV8](https://github.com/Qengineering/YoloV8-ncnn-Raspberry-Pi-4) | 640x640 small | 44.9 | 4.5 | 1.47 | 11.0 | 9.2 | 28.5 | 8.9 |||
| [YoloX](https://github.com/Qengineering/YoloX-ncnn-Raspberry-Pi-4) | 416x416 nano | 25.8 | 22.6 | 7.0 | 34.2 | 28.5 | ||||
| [YoloX](https://github.com/Qengineering/YoloX-ncnn-Raspberry-Pi-4) | 416x416 tiny | 32.8 | 11.35 | 2.8 | 21.8 | 18.1 | ||||
| [YoloX](https://github.com/Qengineering/YoloX-ncnn-Raspberry-Pi-4) | 640x640 small | 40.5 | 3.65 | 0.9 | 9.0 | 7.5 | 30.0 | 10.0 |||

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
$ wget https://github.com/Qengineering/YoloV5-ncnn-Raspberry-Pi-4/archive/refs/heads/main.zip <br/>
$ unzip -j master.zip <br/>
Remove master.zip, LICENSE and README.md as they are no longer needed. <br/> 
$ rm master.zip <br/>
$ rm LICENSE <br/>
$ rm README.md <br/> <br/>
Your *MyDir* folder must now look like this: <br/> 
parking.jpg <br/>
busstop.jpg <br/>
YoloV5.cpb <br/>
yoloV5.cpp <br/>
yolov5s.bin <br/>
yolov5s.param <br/>

------------

## Running the app.
To run the application load the project file YoloV5.cbp in Code::Blocks. More info or<br/> 
if you want to connect a camera to the app, follow the instructions at [Hands-On](https://qengineering.eu/deep-learning-examples-on-raspberry-32-64-os.html#HandsOn).<br/><br/>
Many thanks to [nihui](https://github.com/nihui/) again!<br/><br/>
![output image]( https://qengineering.eu/images/test_busV5.jpg )

------------

[![paypal](https://qengineering.eu/images/TipJarSmall4.png)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=CPZTM5BB3FCYL) 


