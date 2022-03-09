# STM32F10X Platform Library

This is the STM32F10X Platform Library with just the needed code for the DVM hotspot firmware project.

The source of this package can be found here:
https://github.com/STMicroelectronics/STM32CubeF1

In order to run the DVM hotspot firmware correctly, there are the following modifications
already done in this package:

1) STM32F10X_Lib/Device/startup/startup_stm32f10x.c :
    - Added C++ global constructors support
    - Changed initial stack pointer

2) STM32F10X_Lib/Device/stm32f10x_conf.h :
    - Peripheral header file inclusions

3) STM32F10X_Lib/usb
    - Maple Serial-USB support (Virtual COM), only for STM32F103 devices. Most of this code comes from Roger Clark's STM32Duino project. There are modifications in order to use the latest ST libraries. Also, this USB library includes Roger's fix to run this project with USB in Windows.

4) STM32F10X_Lib/utils
    - The binary bootloader and utilities in this folder are from Roger Clark's STM32duino project (https://github.com/stm32duino).

