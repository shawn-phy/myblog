--- 
layout: post
author: Shawn Phy
--- 

# freeRTOS on RP2040 board with vscode
this is a basic tutorial which will show how to setup VScode to be able to compile link and use freeRTOS in pico 
## Introduction 
in the first example we will use a blink program 

#### template repo link 
``` shell 
git clone --recurse-submodules https://github.com/LearnEmbeddedSystems/rp2040-freertos-project
```
#### folder structure 
this is the general structure of the folders 
![image](folders.png)

next we clone the freertos kernel 
``` shell 
git clone https://github.com/FreeRTOS/FreeRTOS-Kernel
```
## CMakeLists Files 
There are three CMakeLists files that we have to create in order to build our project. Please note that if you change any of the folder names then their corresponding entries in the CMakeList.txt files must also be changed.

### parent cmake file 
I have called this “CmakeLists.txt” file the “parent” file as it is located in the top project file.

# communicating with pico serial 
the next project in the series is how to communicte over serial USB to the Pico
this is inspired for [learnembeddedsystems](https://learnembeddedsystems.co.uk)

## Introduction 
Using a serial monitor over USB means that you can essentially output data from your Pico to your PC. It is a very similar process to using the serial monitor on your Arduino.

In this tutorial we are going modify our blink LED code that we made in a previous tutorial. We are going to output a string over USB to further indicate when the LED is on or off. Obviously, you can use the technique we describe here to print to whatever you want in your projects to the serial port.

I am working on a windows machine and so we will need some kind of serial monitor application to monitor the COM port that the Pico will communicate over. I will use PuTTY, and you can download it from their website linked in the description. You can also use the Arduino IDE serial monitor if you have it installed.

## Configuring CMakeLists.txt
So lets open Visual Studio code. Open a developer command prompt by using the windows search, then open Visual studio code using the code command. Navigate to the folder where you have stored your project, if you haven’t set one up then follow the tutorial, linked here, which will show you how to set up a project.

The first change we need to do is in the CMakeLists file. We need to tell the compiler that we are going to be using the USB output and to disable the UART output. This is done with the following:

``` c
pico_enable_stdio_usb(blink_led 1)
pico_enable_stdio_uart(blink_led 0)
``` 
## Writing our C file
In our C file we will wirte the following 
``` c 
#include <stdio.h>
```
Then the first action we need to do in our main function is to call the following function:

``` c
stdio_init_all();
``` 
