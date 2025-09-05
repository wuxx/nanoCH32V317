nanoCH32V305
-----------
[中文](./README_cn.md)

* [Introduce](#Introduce)
* [Feature](#feature)
* [Chip Resources](#chip-resources)
* [How To Use](#how-to-use)
* [Product Link](#product-link)
* [Reference](#reference)


# Introduce
The nanoCH32V317 development board is designed by MuseLab based on the Qinheng CH32V317WCU6 chip. It supports peripherals such as USB2.0 high-speed/Ethernet MAC controller, 10/100M physical layer transceiver, DVP, SDIO, and advanced motor PWM timer. The chip's maximum clock frequency is 144MHz, and it can be downloaded and programmed through the TYPE-C USB port, facilitating rapid prototype verification and development for customers  

![1](https://github.com/wuxx/nanoCH32V317/blob/main/doc/CH32V317-1.jpg)
![2](https://github.com/wuxx/nanoCH32V317/blob/main/doc/CH32V317-2.jpg)

# Feature
- Dual USB interface, USB1 is USB-FS device, USB2 is USB-HS device
- Can be downloaded directly via USB without additional downloader
- Onboard 100M Ethernet interface (with filter)

# Chip Resources
![CH32V317](https://github.com/wuxx/nanoCH32V317/blob/main/doc/CH32V317.png)

# How To Use
## MounRiver Studio IDE
WCH officially provides MounRiver Studio IDE development environment, which supports Windows/Linux/Mac. The instructions are as follows
 
### MounRiver Studio Download
download the MounRiver Studio IDE from the official website [MounRiver Studio](http://www.mounriver.com), and just select the latest version to download.

### Compile
Take the GPIO project as an example, double-click GPIO_Toggle.wvproj to open the project
![MRS-1](https://github.com/wuxx/nanoCH32V317/blob/main/doc/MounRiver-1.png)
Click Project -> Build Project to compile the project  
![MRS-2](https://github.com/wuxx/nanoCH32V317/blob/main/doc/MounRiver-2.png)
Click Flash -> Configuration to configure the target MCU
![MRS-3](https://github.com/wuxx/nanoCH32V317/blob/main/doc/MounRiver-3.png)


## Program via SWD Interface
If use WCH's official downloader WCHLink, connect the wires as follows
WCHLink|nanoCH32V317 |
----|----|
GND |  GND |
SWCLK | PA14 |
SWDIO | PA13 |
3V3 | 3V3|

then Click Flash -> Download to program the MCU  
![MRS-4](https://github.com/wuxx/nanoCH32V317/blob/main/doc/MounRiver-4.png)


Note: The compiled binary file is located in the obj directory of the project, such as EVT\EXAM\GPIO\GPIO_Toggle\obj\GPIO_Toggle.hex

## Program via USB ISP
### WCHISPStudio Download
download WCHISPStudio at [WCH Official Website](https://www.wch.cn/downloads/WCHISPTool_Setup_exe.html)

### WCHISPStudio Config
![ISP-1](https://github.com/wuxx/nanoCH32V317/blob/main/doc/WCHISPStudio-EN-1.png)

The chip series select CH32V31x series, the chip model select CH32V317WCU6, and the download method select USB.
Keep pressing the BOOT button on the development board, then press and release the RST button, and finally release the BOOT button to make the chip enter the bootloader. If the bootloader is successfully entered, the target can be detected in the USB device list in the WCHISPStudio.
Then select the bin or hex file to be programmed, and click Download to burn the firmware.
![ISP-2](https://github.com/wuxx/nanoCH32V317/blob/main/doc/WCHISPStudio-EN-2.png)
![ISP-3](https://github.com/wuxx/nanoCH32V317/blob/main/doc/WCHISPStudio-EN-3.png)

# Product Link
[Aliexpress](https://www.aliexpress.com/item/1005005033298927.html?spm=a2g0s.12269583.0.0.20535947csm0Sw
)
[Tindie](https://www.tindie.com/products/johnnywu/nanoch32v305-development-board/)

# Reference
### WCH
[https://www.wch.cn/](https://www.wch.cn/)
### MounRiver
[http://www.mounriver.com](http://www.mounriver.com)
