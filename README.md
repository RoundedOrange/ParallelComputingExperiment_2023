# 山东大学2023多核平台下的并行计算实验

## 组员

郑嘉骏 大数据1班 202000300349

姜将 大数据1班 202018202224

胡珂铭 大数据2班

## 运行前准备

1. C++编译器

题目要求使用gcc8.3版本及以上版本编译器。在终端输入```gcc -v```来检查编译器是否是恰当版本。

## 如何运行

1. 通过```make```命令编译。
2. 在linux下通过```./main.exe <thread_num>```来运行。如果想要个性化实际的参数，则使用```./main.exe <thread_num> <number_bands> <nv_bands> <ncouls> <nodes_per_group>```。例如，想要用32线程运行程序，则用```./main.exe 16```。如果想要32线程,number_bands=512,nvband = 2,ncouls = 32768,nodes_per_group = 20的参数下运行，则使用```./main.exe 32 512 2 32768 20```运行。
3. 在Windows下通过```.\main.exe <thread_num>```来运行。linux和Windows平台斜杠和反斜杠有些许差别。

## 用时

在CPU为i7-13700KF（16核24线程），系统为Windows10的环境上运行程序，不同线程的用时如下。
|线程|Kernel用时（秒）|Total用时（秒）|总用时的加速比|
|:-:|:-:|:-:|:-:|
|1|54.3182|54.8251|1.0|
|2|28.7097|29.1592|1.8802|
|4|27.6508|28.0933|1.9515|
|8|7.85286|8.2945|6.6098|
|16|5.99294|6.44185|8.5108|
|32|5.49899|5.94489|9.2222|
|64|5.2105|5.65249|9.6993|
