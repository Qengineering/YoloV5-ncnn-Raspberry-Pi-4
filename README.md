# YoloV5-ncnn-Raspberry-Pi-4
![output image]( https://qengineering.eu/images/test_parkV5.jpg )
## YoloV5 with the ncnn framework. <br/>
[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)<br/><br/>
Paper: https://towardsdatascience.com/yolo-v5-is-here-b668ce2a4908<br/><br/>
Special made for a bare Raspberry Pi 4, see [Q-engineering deep learning examples](https://qengineering.eu/deep-learning-examples-on-raspberry-32-64-os.html)

------------

## Benchmark.
| Model  | Jetson Nano 2015 MHz | RPi 4 64-OS 1950 MHz |
| ------------- | :-------------:  | :-------------: |
| YoloV2 (416x416)      |  10.1 FPS | 3.0 FPS |
| YoloV3 (352x352) tiny |  17.7 FPS | 4.4 FPS |
| YoloV4 (416x416) tiny |  11.2 FPS | 3.4 FPS |
| YoloV4 (608x608) full |  0.7 FPS | 0.2 FPS |
| YoloV5 (640x640) small|  4.0 FPS | **1.6 FPS** |

------------

## Dependencies.
To run the application, you have to:
- A raspberry Pi 4 with a 32 or 64-bit operating system. It can be the Raspberry 64-bit OS, or Ubuntu 18.04 / 20.04. [Install 64-bit OS](https://qengineering.eu/install-raspberry-64-os.html) <br/>
- The Tencent ncnn framework installed. [Install ncnn](https://qengineering.eu/install-ncnn-on-raspberry-pi-4.html) <br/>
- OpenCV 64 bit installed. [Install OpenCV 4.5](https://qengineering.eu/install-opencv-4.5-on-raspberry-64-os.html) <br/>
- Code::Blocks installed. (```$ sudo apt-get install codeblocks```)

------------

## Installing the app.
To extract and run the network in Code::Blocks <br/>
$ mkdir *MyDir* <br/>
$ cd *MyDir* <br/>
$ wget https://github.com/Qengineering/YoloV5-ncnn-Raspberry-Pi-4/archive/refs/heads/master.zip <br/>
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
To run the application load the project file YoloV5.cbp in Code::Blocks.<br/> 
Next, follow the instructions at [Hands-On](https://qengineering.eu/deep-learning-examples-on-raspberry-32-64-os.html#HandsOn).<br/><br/>
Many thanks to [nihui](https://github.com/nihui/) again!<br/>
![output image]( https://qengineering.eu/images/test_busV5.jpg )

