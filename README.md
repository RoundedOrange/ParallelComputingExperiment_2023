# 山东大学2023多核平台下的并行计算实验

## 组员

郑嘉骏 大数据1班 202000300349

姜将 大数据1班 202018202224

胡珂铭 大数据2班 202000300401

## 运行前准备

1. C++编译器

题目要求使用gcc8.3版本及以上版本编译器。在终端输入```gcc -v```来检查编译器是否是恰当版本。

2. Makefile

## 如何运行

1. 通过```make```命令编译。如果是在Windows平台上的话记得把对应的make程序添加到系统路径PATH。Linux平台好像是自带的，不用进行其他操作。
2. 在linux下通过```./main.exe <thread_num>```来运行。如果想要个性化实际的参数，则使用```./main.exe <thread_num> <number_bands> <nv_bands> <ncouls> <nodes_per_group>```。例如，想要用32线程运行程序，则用```./main.exe 16```。如果想要32线程,number_bands=512,nvband = 2,ncouls = 32768,nodes_per_group = 20的参数下运行，则使用```./main.exe 32 512 2 32768 20```运行。
3. 在Windows下通过```.\main.exe <thread_num>```来运行。linux和Windows平台斜杠和反斜杠有些许差别。
4. 推荐使用16、32、64线程运行，因为线程数太少的话可能速度比较慢。

## 用时

在CPU为i7-13700KF（16核24线程），系统为Windows10的环境上运行程序，不同线程的用时如下。
|线程|Kernel用时（秒）|Total用时（秒）|总用时的加速比|
|:-:|:-:|:-:|:-:|
|1|47.8222|48.2534|1.0|
|2|23.8569|24.2909|1.9865|
|4|12.5885|13.0168|3.7070|
|8|6.48135|6.91353|6.9796|
|16|5.61147|6.05093|7.9745|
|32|5.14712|5.58705|8.6367|
|64|4.85308|5.29001|9.1216|
