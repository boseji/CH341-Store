# CH341-Store
Documents and Software Related to the famous CH341a used in I2C/SPI Flash Programmers also called as BIOS Programmers

Please note that this repository is a Coagulation of know-how from different sources.

![CH341A Devices](https://1.bp.blogspot.com/-RFzfABqVamg/WlEZ-s0FkxI/AAAAAAAAIqg/3L0JBCCQN9sNm4e7ST9Csczwwu7tO1OzgCLcBGAs/s1600/ch341a_products.png)
> Source : https://www.onetransistor.eu/2017/08/ch341a-mini-programmer-schematic.html

## About CH341

This is versatile USB to multi-protocol converter chip.

There are 4 major items that become clear from the enclosed **[Datasheet(English)](https://github.com/boseji/CH341-Store/raw/master/CH341_EN.pdf)**

  * UART - The chip can be used as a USB to UART converter. It can also be used for RS-485 since it has automatic driver control pin also available.
  * Synchronous Serial - I2C and SPI - The chip has 3 chip select pins and Multi-mode support for SPI protocol. Also the chip has dedicated I2C pins.
  * Parallel Interface - This interface can be used to talk to parallel memory Bus with all the required control signals
  * Printer Port - The device can emulate a EPP Parallel Port over USB to be able to connect to older printers .etc.

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
  * [**Alexander Gavrilov**](https://github.com/dartraiden) - Provided us with the following insight:
    - OpenSource usbASP Flash Programmer .aka. **AsProgrammer** https://github.com/nofeletru/UsbAsp-flash
      *Windows GUI Based programmer significantly better performance than closed-source version* see [Issue #5](https://github.com/boseji/CH341-Store/issues/5#issuecomment-574433239)
    - Avrdude version supporting CH341a https://github.com/Alx2000y/avrdude_ch341a
    - Ch341Programmer - Closed Source Links: http://televid-sib.ru/index.php?topic=42039.msg161311;topicseen#msg161311
    - Colibri - Closed Source Links: http://apkservice.ru/articles/page,1,7,28-soft-dlya-programmatora-na-ch341a.html
    - Postal3 - Closed Source Links: https://monitor.net.ru/forum/threads/436716/
    - postal3_ch341 - Closed Source Links: http://docs.expressvl.ru/postal3_ch341.html
  * Github User [BigBox2020](https://github.com/BigBox2020) has provided us with **flashrom**
    instructions and some closed-source programming options.
    Here are the contributions:
    - *ch341a programmer v1.13* https://drive.google.com/file/d/0ByEQKtsOckWBUVBqajZOUGtLcnM/view
    - [Video Tutorial](https://www.youtube.com/watch?v=L0ChYNwunUE) on how to use *ch341a programmer v1.13*
      https://www.youtube.com/watch?v=L0ChYNwunUE
    - **flashrom** Tutorial for Windows https://www.win-raid.com/t796f16-Guide-Using-CH-A-based-programmer-to-flash-SPI-EEPROM-5.html#msg41915
    - *How to do **HP PAVILION 500-0XX/ENVY 700-0XX BIOS RECOVERY*** https://vdhout.nl/2018/02/hp-pavilion-500-0xx-envy-700-0xx-bios-recovery
    - Github User [BigBox2020](https://github.com/BigBox2020) has been kind enough to provide us with the Virus report
      of the above packages.
    - Virus total report for *ch341a programmer v1.13* https://www.virustotal.com/gui/file/0b6aba1bfa041ea3484cb4e6750427de468ece553a9461dba388fee16ad3669a/detection
    - Virus total report for **flashrom** windows 
    https://www.virustotal.com/gui/file/0eb1e5cde08fa44e015c5b56d01e330078a32b4efad4336513ee789f974b559c/detection

## CH341a based Programmer

The Main uses that this chip finds is programing SPI flash chips. These SPI flash chips are often used in the BIOS of many computer cards. In fact most of the WiFi routers use these SPI flash chips to store the embedded Linux image. So ideally these programmers can actually help you swap the Linux image on a WiFi Router. Also it has been reported that this programmer can be used to recover bricked or locked out BIOS from laptops.

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

~~We still did not find any clean programmer application, that does
not contain any viruses. Hence if any one can help us provide a clean
programmer application - please let us know.~~

We have finally found one piece of closed source software for programming.
This was contributed by Github User [BigBox2020](https://github.com/BigBox2020).
Another is usbASP Flash Programmer .aka. **AsProgrammer**. This is an 
*Open-Source* alternative contributed by [Alexander Gavrilov](https://github.com/dartraiden).

Please find the links to the respective contributions below.

Here are few Open-source projects targeting this platform:

 - https://github.com/setarcos/ch341prog
 - https://github.com/stefanct/ch341eepromtool
 - https://www.flashrom.org/Flashrom

### Contribution by [*Alexander Gavrilov*](https://github.com/dartraiden)

Here are few more Open-Source projects shared with us by [*Alexander Gavrilov*](https://github.com/dartraiden)

  - OpenSource usbASP Flash Programmer .aka. **AsProgrammer** https://github.com/nofeletru/UsbAsp-flash
    > [*Alexander Gavrilov*](https://github.com/dartraiden) has confirmed that **AsProgrammer** is *very*
    > *common among the Russian users*. This has a *good GUI and works better than the closed source version*
    > as per [Issue #5](https://github.com/boseji/CH341-Store/issues/5#issuecomment-574433239).
  - Avrdude version supporting CH341a https://github.com/Alx2000y/avrdude_ch341a

Here are a few Close-Source links shared with us by [*Alexander Gavrilov*](https://github.com/dartraiden)

  - Ch341Programmer http://televid-sib.ru/index.php?topic=42039.msg161311;topicseen#msg161311
  - Colibri http://apkservice.ru/articles/page,1,7,28-soft-dlya-programmatora-na-ch341a.html
  - Postal3 https://monitor.net.ru/forum/threads/436716/
  - postal3_ch341 http://docs.expressvl.ru/postal3_ch341.html

### Contribution by Github User [BigBox2020](https://github.com/BigBox2020)

Here are a few Closed-Source links shared with us by Github User [BigBox2020](https://github.com/BigBox2020):

 - **Ch341 programmer v1.13** https://drive.google.com/file/d/0ByEQKtsOckWBUVBqajZOUGtLcnM/view
 - Video Tutorial on using **Ch341 programmer v1.13** https://www.youtube.com/watch?v=L0ChYNwunUE
 - **Ch341 programmer v1.13** has been verified using Virus Total service:
   https://www.virustotal.com/gui/file/0b6aba1bfa041ea3484cb4e6750427de468ece553a9461dba388fee16ad3669a/detection

Here are a few Open-Source tool **flashrom** links shared with us by Github User [BigBox2020](https://github.com/BigBox2020):

 - **flashrom** for windows Tutorial and package 
   https://www.win-raid.com/t796f16-Guide-Using-CH-A-based-programmer-to-flash-SPI-EEPROM-5.html#msg41915
 - *How to do **HP PAVILION 500-0XX/ENVY 700-0XX BIOS RECOVERY*** https://vdhout.nl/2018/02/hp-pavilion-500-0xx-envy-700-0xx-bios-recovery
  - Note that the **flashrom** has been verified using Virus total:
    https://www.virustotal.com/gui/file/0eb1e5cde08fa44e015c5b56d01e330078a32b4efad4336513ee789f974b559c/detection

## Help Needed

Please feel free to contribute anything you believe would be helpful for the community.

Current parts that need help:
1. **Verifying closed source *CH341a Programmer Application* listed** Last time we removed the items since community complained of virus contained in some distributions. We request help to verify the programmer solutions are safe to use before hosting them here.
2. **Translation** We need help with correct translation of documentation. This might be from other languages to common English.
3. **Tutorials** We need help with tutorials for building and using Open Source or Closed-Source applications for *CH341a Programmer Application*.



  
