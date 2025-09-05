nanoCH32V317
-----------
[English](./README.md)

* [nanoCH32V317介绍](#nanoCH32V317介绍) 
* [特性](#特性)
* [芯片资源](#芯片资源)
* [使用教程](#使用教程)
* [产品链接](#产品链接)
* [参考](#参考)


# nanoCH32V317介绍
nanoCH32V317开发板是MuseLab基于沁恒CH32V317WCU6芯片设计的的开发板，支持USB2.0高速/以太网MAC控制器及10/100M物理层收发/DVP/SDIO/电机PWM高级定时器等外设，芯片最高主频144MHz，可通过TYPE-C USB口下载烧录，方便客户进行快速的原型验证及开发  

![1](https://github.com/wuxx/nanoCH32V317/blob/master/doc/CH32V317-1.jpg)
![2](https://github.com/wuxx/nanoCH32V317/blob/master/doc/CH32V317-2.jpg)


# 特性
- 双USB接口，其中USB1为USB-FS设备，USB2为USB-HS设备
- 通过USB ISP下载或者SWD接口下载
- 板载8MHz与32.768K晶振
- 板载百兆以太网接口(带滤波器)

# 芯片资源
![CH32V317](https://github.com/wuxx/nanoCH32V317/blob/master/doc/CH32V317.png)

# 使用教程
## MounRiver Studio IDE
沁恒官方提供MounRiver Studio IDE开发环境，支持Windows/Linux/Mac，具体使用说明如下
 
### MounRiver Studio 下载
可在官网[MounRiver Studio](http://www.mounriver.com)下载IDE，选择最新版本下载即可。

### 编译
以GPIO工程为例，双击GPIO_Toggle.wvproj打开工程  
![MRS-1](https://github.com/wuxx/nanoCH32V317/blob/master/doc/MounRiver-1.png)
![MRS-2](https://github.com/wuxx/nanoCH32V317/blob/master/doc/MounRiver-2.png)  
点击 Project -> Build Project 对工程进行编译  
![MRS-3](https://github.com/wuxx/nanoCH32V317/blob/master/doc/MounRiver-3.png)


## SWD烧录
若使用沁恒官方的下载器WCHLink进行下载，则按照如下方式接线
WCHLink|nanoCH32V317 |
----|----|
GND |  GND |
SWCLK | PA14 |
SWDIO | PA13 |
3V3 | 3V3|

然后则点击MounRiver界面上的菜单 Flash -> Download 即可完成烧录，若使用自带的USB口进行烧录，则操作说明如下
![MRS-4](https://github.com/wuxx/nanoCH32V317/blob/master/doc/MounRiver-4.png)

注：编译生成的二进制文件位于工程的obj目录下，如EVT\EXAM\GPIO\GPIO_Toggle\obj\GPIO_Toggle.hex

## ISP烧录
### WCHISPStudio 下载
可在[沁恒官网](https://www.wch.cn/downloads/WCHISPTool_Setup_exe.html)下载WCHISPTool工具

### WCHISPTool 配置
![ISP-1](https://github.com/wuxx/nanoCH32V317/blob/master/doc/WCHISPStudio-CN-1.png)

芯片系列选择CH32Vx系列，芯片型号选择CH32V317，下载方式选择USB。
持续按住开发板上的BOOT按键，然后按下RST按键并松开，最后再松开BOOT按键，令芯片进入bootloader，若成功进入bootloader，则在ISP工具中的USB设备列表中可检测到目标芯片。
然后在下方选择需要烧录的bin或者hex文件，点击下载即可烧录固件。
![ISP-2](https://github.com/wuxx/nanoCH32V317/blob/master/doc/WCHISPStudio-CN-2.png)
![ISP-3](https://github.com/wuxx/nanoCH32V317/blob/master/doc/WCHISPStudio-CN-3.png)

# 产品链接
[nanoCH32V317 Board](https://item.taobao.com/item.htm?abbucket=9&id=972476111665)

# 参考
### WCH
[https://www.wch.cn/](https://www.wch.cn/)
### MounRiver
[http://www.mounriver.com](http://www.mounriver.com)
