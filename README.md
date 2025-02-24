# resources
Provides documentation and BSP images for the Leez Single Board Computer products.
## 产品概述

**Leez P710硬件规格书（包括接口布局和尺寸）**
* 链接：https://github.com/leezsbc/resources/blob/master/%E6%A0%97%E5%AD%90%E6%9D%BFP710%E7%A1%AC%E4%BB%B6%E8%A7%84%E6%A0%BC%E4%B9%A6V1.1.pdf

**Leez P710原理图**
* 链接: https://pan.baidu.com/s/1NPWbuI5csT4zftKUCnRs7g 
* 提取码: rvrh 

**入门教程**
* 链接：https://github.com/leezsbc/resources/blob/master/Leez%20P710%E5%88%B7%E6%9C%BA%E6%96%87%E6%A1%A3.docx


## 固件烧写

**Leez P710二次开发指南**
* 链接：
https://github.com/leezsbc/resources/blob/master/Leez%20P710%E4%BA%8C%E6%AC%A1%E5%BC%80%E5%8F%91%E6%8C%87%E5%8D%97%20-%20v1.0.pdf


## 刷机工具

**DriverAssitant_v4.5_设备驱动**
* 链接：https://pan.baidu.com/s/15pvlJSZF6jX2ZaKZnW5bcg 
* 提取码：hjbc 

**FactoryTool_v1.63_eMMC镜像刷写**
* 链接：https://pan.baidu.com/s/1eWvCKhM1iIto86fMmmZ5XA 
* 提取码：ir3z 

**SDDiskTool_v1.57_SD卡镜像刷写（Windows环境）**
* 链接：https://pan.baidu.com/s/13XCiqUV_fp_MvpsNtNy3Uw 
* 提取码：jmt1 

**SDDiskTool_v1.57_SD卡镜像刷写（Linux环境）**
* 链接: https://pan.baidu.com/s/1wLlexYUMQGUFkW2zSWT1YA 
* 提取码: mg3a

## OS Images

**Android9.0_LZP_V003**
* 链接：https://pan.baidu.com/s/1gTyc84xxchffx04eQHg8tA 
* 提取码：rrs9 

**DebianFS_Leez**
* 链接：https://pan.baidu.com/s/1zuHdeSB5fSz9P5MOBofjmQ 
* 提取码：2xyj

## 常见Q&A

**1. 如何正确格式化TF卡？**
* 建议使用官方提供的SD disk tool v1.57工具进行格式化， 用其他方式（例如在windows/linux/android系统中）格式化，可能会带来重启死机、显示容量与标称容量不一致等问题。

**2. 如何处理在Android7.1下，TF卡格式化后的异常现象？**
* 在使用SD disk tool v1.57工具对超过32GB容量（不含32GB）的TF卡进行格式化，在Android9.0系统下，TF卡容量显示正常。而目前Android7.1系统下，显示的TF卡容量为4M，请注意此情况是RK的格式化工具的问题，虽然TF卡容量显示不正常，但是不影响TF卡在该系统下的正常使用。

**3. 如果eMMC和TF卡上都有系统，优先启动哪一个？**
* 系统启动顺序为”TF卡优先”。

**4. Android7.1支持从TF卡启动吗？**
* 不支持。

**5. Android9.0支持从TF卡启动吗？**
* 支持。

**6. Android9.0在TF卡与eMMC同时启动系统会遇到失败问题。**
* 当TF卡上装有Android9.0, 且eMMC也同时装了可启动的系统时，系统启动会失败，这是当前Rockchip的limitation。

**7. 如何切换音频输出？**
* Leez P710连接HDMI显示器，以及通过USB Type C接口连接的显示器，默认会优先于耳际插座输出声音（闹钟功能除外）。如果需要将声音切换到非默认的声音输出设备，可以使用第三方软件进行切换，例如Soundabout软件. 

**8. Leez P710有MIC模块吗？**
* 板子未安装模拟MIC, 需要此功能的用户可自行安装模拟MIC或I2S外置声卡模块。

**9. 系统亮度调节功能可以调节所有显示器吗？**
* 亮度调节功能只能调节Mipi接口显示器，HDMI/DP的亮度不受系统控制。

**10. 如何处理系统显示时间不一致的问题？**
* 在Android9.0下，系统启动解锁登录界面显示的时间和进入系统后的时间显示不一致. 这是Android9.0的limitation, 此问题不影响系统下的功能。解锁进入系统后，时间恢复正常。如果需求正确显示，可将在二次开发时将该界面显示的时间改为不显示。

**11. 产品支持双屏显示不同内容吗？**
* 产品默认支持双屏同显，如果需要双屏异显，需要深度开发。

**12. 如何使用产品的双摄像头功能？**
* 产品默认支持双摄像头同时信息采集，需使用官方开发支持的软件（如需提供，请Leezinfo@lenovo.com联系管理员）。如果需要双摄像头拍照和录像，需要用户自行开发。

**13. 为什么录像到一定时间会终止？**
* 录像过程中，当录像视频文件超过3.8GB时，录像会自动终止。因为受限于FAT32,及录像缓存，产品默认录像到3.8G左右时自动停止。如需解除录像限制，需要进行二次开发。

**14. 目前Leez P710支持哪些相机模组？**
* MIPI: CAM1320； USB: UVC协议。

**15. 目前Leez P710支持哪些4G模组？**
* Quectel：EM05
* 注意事项：
EM05有两种版本，一种是标准版本，默认是MBIM，主要是用在win10上。一种是ND版本，默认NDIS方式，可以用在win7和Android上。EM05的MBIM是针对Windows平板开发的，产品定义也是给windows使用，Linux上推荐使用qmi_wwan后缀_ND的固件，可支持QMI/MBIM两种模式。如果固件是EM05CEFAR01A04M4G，要升级为EM05CEFAR01A04M4G_ND，并保证Usbnet mode 是QMI。

**16. 目前Leez P710支持哪些TF卡？**
* Samsung 32G TF C10；Samsung 64G TF C10；Samsung 128G TF C10；SanDisk 32G TF C10；SanDisk 64G TF C10；SanDisk 128G TF C10
