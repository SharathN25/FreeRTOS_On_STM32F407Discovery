# FreeRTOS on STM32F407 Discovery Kit

## FreeRTOS

A **Real-Time Operating System(RTOS)**  is a software that is specifically designed to run applications with very **precise timing** and a high degree of **reliability**. Almost all real-time operating systems provide threading, the illusion that processors can execute many tasks at the same time. Real-time software is ideal for deadline-specific systems. It ensures that the prediction of tasks execution durations is done accurately.

The **[FreeRTOS](https://www.freertos.org/)** is a real-time operating system kernel for embedded devices that has been ported to 35 microcontroller platforms. FreeRTOS is designed to be small and simple. The kernel itself consists of only three C files. To make the code readable, easy to port, and maintainable, it is written mostly in C, but there are a few assembly functions included where needed (mostly in architecture-specific scheduler routines). You can get freeRTOS here [Download FreeRTOS](https://www.freertos.org/a00104.html).

## STM32F407 Discovery Kit
The STM32F407 Discovery Board is a Microconctroller which is based on ARM Cortex-M4 Architecture. If you want to know about this MUC there is a detailed project made on how to use this MCU with all necessary information to get started here [STM32F407-Discovery](https://github.com/SharathN25/STM32F407-Discovery)

## Running FreeRTOS on STM32F407 Discovery Kit
The first step is to download the **FreeRTOS**. Once you have donwloaded the FreeRTOS source files make sure you copy them into your project folder. Here I will be using **Keil uVision 5** IDE to set up freeRTOS.  You can find detailed step to set up FreeRTOS below:

* **[Setting Up FreeRTOS](https://github.com/SharathN25/FreeRTOS_On_STM32F407Discovery/tree/master/Seeting%20up%20FreeRTOS)** - Detailed steps do the initial FreeRTOS setup in Keil uVision 5.


