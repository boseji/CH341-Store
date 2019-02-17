# CH341-Store
Documents and Software Related to the famous CH341a used in I2C/SPI Flash Programmers also called as Bios Programmers

Please note that this repository is a Coagulation of know-how from diffrent sources.

![CH341A Devices](https://1.bp.blogspot.com/-RFzfABqVamg/WlEZ-s0FkxI/AAAAAAAAIqg/3L0JBCCQN9sNm4e7ST9Csczwwu7tO1OzgCLcBGAs/s1600/ch341a_products.png)
> Source : https://www.onetransistor.eu/2017/08/ch341a-mini-programmer-schematic.html

## About CH341

This is versetaile USB to multi-protocol converter chip.

There are 4 major items that becoe clear from the enclosed **[Datasheet(English)](https://github.com/boseji/CH341-Store/raw/master/CH341_EN.pdf)**

  * UART - The chip can be used as a USB to UART converter. It can also be used for RS-485 since it has automatic driver convtrol pin also available.
  * Synchronous Serial - I2C and SPI - The chip has 3 chip selct pins and Multi-mode support for SPI prototocol. Also the chip has dedicated I2C pins.
  * Parallel Interface - This interface can be used to talk to parallel memory Bus with all the required control signals
  * Printer Port - The deivice can emulate a EPP Parallel Port over USB to be able to connect to older printers .etc.

## Attributions

  * **OneTransistor** https://www.onetransistor.eu/ - Good website if you are looking for electronics ideas and many Maker topics.
    - More Specifically the Article : https://www.onetransistor.eu/2017/08/ch341a-mini-programmer-schematic.html . A PDF version of this article is available here.
    - How to use CH341A to Program a **Arduino-Pro Mini** : https://www.onetransistor.eu/2018/02/program-arduino-pro-mini-with-ch341a.html
    - Windows API for I2C Programming : https://www.onetransistor.eu/2017/09/ch341a-usb-i2c-programming.html
    - Windows API for SPI Programming : https://www.onetransistor.eu/2017/12/ch341a-usb-spi-programming.html
  * **Electrodragon** https://www.electrodragon.com - One of the best Maker shops out there, you can find tons of goodies for your projects
    - Very useful breakout board for CH341a Chip: https://www.electrodragon.com/product/ch341-usb-convert-flash-board-usb-ttl-iic-spi-etc/
    - Documentation about the board: https://www.electrodragon.com/w/CH340
  * ***Jiangsu QinHeng Ltd*** Company creating these wonderful CH341a ICs http://www.wch.cn/
    - Translated Version of the Website: https://translate.google.com/translate?hl=en&sl=zh-CN&u=http://wch.cn/
    - Product Page of **CH341a** IC : https://translate.google.com/translate?depth=1&hl=en&rurl=translate.google.com&sl=zh-CN&sp=nmt4&u=http://www.wch.cn/products/CH341.html
    
## CH341a based Programmer

The Main uses that this chip finds is programing SPI flash chips. These SPI flash chips are ofen used in the BIOS of many computer cards. Infact most of the WiFi routers use these SPI flash chips to store the embedded linux image. So ideally these programmers can actually help you swap the linux image on a WiFi Router. Also it has been reported that this programmer can be used to recover bricked or locked out Bios from laptops.

Lets look at how the programmer looks like:

![Typical CH341 based programmer](https://2.bp.blogspot.com/-gweW5sI33Jo/WYXq-vJAEbI/AAAAAAAAHHE/MXFTaSMgVtkn7ueKZdjpzoOu0i7tV_pJQCLcBGAs/s1600/ch341aminiprog.jpg)
> Source: https://www.onetransistor.eu/2017/08/ch341a-mini-programmer-schematic.html

Folks at **[Onetransistor](https://www.onetransistor.eu)** have been kind enough to provide a schematics also:

![Schematics of a CH341 based programmer](https://github.com/boseji/CH341-Store/raw/master/ch341a_miniprogrammer_schematic.png)
> Source: https://www.onetransistor.eu/2017/08/ch341a-mini-programmer-schematic.html

![PCB of a CH341 based programmer](https://github.com/boseji/CH341-Store/raw/master/ch341a_pcb.jpg)
> Source: https://www.onetransistor.eu/2017/08/ch341a-mini-programmer-schematic.html

## CH341a Drivers

We have downloaded the drivers from **[Jiangsu QinHeng Ltd Website](http://www.wch.cn/products/CH341.html)** hence all should be Genuine Drivers , malicious items free.

### For Windows

  * **[CH341-Windows-SPI-I2C-Driver+SDK-library/CH341PAR.ZIP](https://github.com/boseji/CH341-Store/raw/master/CH341-Windows-SPI-I2C-Driver%2BSDK-library/CH341PAR.ZIP)** - For the programmer
  * **[CH341-Windows-Serial-Driver+SDK-library/CH341SER.ZIP](https://github.com/boseji/CH341-Store/raw/master/CH341-Windows-Serial-Driver%2BSDK-library/CH341SER.ZIP)** - Serial Driver

### For Linux

Most of the times you would not need any driver specifically since its auto registered.
However to communicate you might need the help of libraries.

 * **[CH341-Linux-SPI-I2C-Driver+SDK-library/CH341PAR_LINUX.ZIP](https://github.com/boseji/CH341-Store/raw/master/CH341-Linux-SPI-I2C-Driver%2BSDK-library/CH341PAR_LINUX.ZIP)** - For the Programmer
 * **[CH341-Linux-Serial-Driver+SDK-library/CH341SER_LINUX.ZIP](https://github.com/boseji/CH341-Store/raw/master/CH341-Linux-Serial-Driver%2BSDK-library/CH341SER_LINUX.ZIP)**

### For Android Devices

It's interesting that the manufacturer actually provides support Android support. Not only that they provide the Android application to test and the Library in `.jar` form.

### For MAC

There is not much support for MAC from the manufacturer.

## CH341a Programmer Application

We still did not find any clean programmer application, that does
not contain any viruses. Hence if any one can help us provide a clean
programmer application - please let us know.
