# TranSec OS
TranSec OS是一个基于Ubuntu 18.04的车联网渗透测试发行版系统，主要用于针对车联网设备进行安全评估。系统内置上百个车联网安全测试专用工具，旨在解决车联网安全从业人员测试工具杂乱、测试环境配置复杂、无工具可用等一系列问题
## 优势
开箱即用的测试环境，包含上百个常见用于车联网渗透测试的工具集。覆盖逆向、CAN、车载以太网、WiFi、蓝牙、云平台等安全测试
- 永久的免费更新支持，后续将逐步增加安恒车联网自研工具及部分商用软件定向免费试用
- 开放的操作环境，允许用户定制修改系统内的任意文件、安装任意程序
- 内置ARM、X86、MIPS等不同架构下各类常用工具，如adb、gdb、nmap、busybox等
- ....

## 工具列表（部分）
以下列出其中部分工具，更多工具大家可自行下载进行探索。
| 工具名称 | 工具介绍 |
| --- | --- |
| CANToolz | CAN分析框架 |
| Can-Utils | can的测试工具集 |
| scapy | 数据包处理工具 |
| Proxmark3 | PM3客户端 |
| Logic | 逻辑分析仪客户端 |
| URH | 无线电分析工具 |
| MQTTclient | MQTT客户端 |
| gattool | BLE连接工具 |
| binwalk | 固件解包与分析工具 |
| IDA Free | 专业的二进制分析工具 |
| Shambles | 专业的二进制分析与漏洞扫描工具 |
| Ghidra | 开源二进制分析工具 |
| Jeb | 安卓逆向分析工具 |
| Jadx-Gui | 开源安卓逆向分析工具 |
| hcitool | 蓝牙连接工具 |
| Ubertooth tools | 一款软硬件开源的蓝牙抓包器 |
| pybluez2 | python库-蓝牙攻击工具 |
| KillerBee | 针对ZigBee的安全研究工具 |
| HackRF | HackRF配套软件 |
| Frida | hook工具 |
| gdb-multiarch | 异架构gdb分析工具 |
| pwndbg | gdb进阶脚本 |
| pwntools | python下漏洞利用框架 |
| qemu | 开源模拟器 |
| qemu-system | 虚拟系统模拟程序 |
| Firmware-Mod-Kit | 固件修改套件 |
| Firmware Analysis Toolkit | 开源的固件分析工具 |
| frp | 内网穿透工具 |
| MobSF | 安卓自动化静态分析工具 |
| Burpsuit | Web测试工具 |

# 下载
- GitHub：https://github.com/TianWen-Lab/TranSec
- 百度网盘：链接:[https://pan.baidu.com/s/1X_Cx5vOprY0ONkLPYHJ2tw](https://pan.baidu.com/s/1X_Cx5vOprY0ONkLPYHJ2tw) 提取码:e475

# 安装说明

本系统提供ISO镜像安装与OVA镜像导入方式安装，推荐使用OVA导入虚拟机操作更为简单方便。由于系统较大导入或安装需要一定时间，具体时间与磁盘性能有关。

导入或安装成功后开机使用`iov/root`进行登录，登录成功后会显示用户体验计划，可选择同意或拒绝，确认完成后即可开始使用。

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/8b3dacaf-7668-4be8-baf4-8c4ebdc3fcaa)

## OVA导入
使用虚拟机软件打开OVA文件即可

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/168420ab-1064-4452-b201-2d67c5b1ae4a)

## ISO安装
使用ISO镜像安装时**建议配置50G磁盘+4G内存**，加载镜像后选择`Boot system install`进入安装流程

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/f51c53c6-bcb1-4d1f-8544-ca87d8f82ac2)

输入`iov/root`密码登录安装界面

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/0c76f57a-528f-4226-a744-fca508b2ed7b)

根据提示输入账号密码等信息，点击下一步进入分区流程。

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/7da9584d-ef52-4b72-93cd-2bdf70803eee)

选择磁盘后点击Delete删除分区

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/e45d4c52-ffe8-43ba-ae1a-709dfb339ccf)

此时会出现一个`/dev/sda?`，选中`/dev/sda?`，点击箭头

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/44e08672-3419-407b-9aaf-6c81442d6213)

此时`/dev/sda?`就变成了`/dev/sda1`，选中这个分区，在右边的菜单中下拉选择挂载的目录（/）和分区格式（ext4），再次点击箭头即可完成分区

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/e2c4dd07-ba00-43a3-afe3-c3a1fbfef60f)


回到安装流程，在勾选包含用户配置和数据（**一定要改成√**）后进行下一步就可以进行安装了

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/9e4a1ae3-65a1-44f0-8a11-1bfed3d1bb07)

安装时间大概6分钟左右，待进度完成后点击reboot完成安装流程并进入系统

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/57042e75-32c0-4cba-b98a-b92dd730aa36)



# 系统内截图
![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/e6d0e230-e90a-48ce-ad69-bb512408c5c7)

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/b564d4f6-18c2-4298-994a-b06d19d2b6b5)

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/a5db4f60-97ff-4c8e-afe4-8437a22e73df)

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/997e4687-0234-4334-a3b8-ff91ef20539e)

# 安装可能出现的问题
由于是基于systemback，所以在安装系统时可能会出现一些问题，下面给出对应的解决方法：

1、使用ISO安装方式，在登录安装界面时弹出“Cannot start the Systemback graphical user interface! Unable to connect to the X server”或其他没有进入到安装界面的原因，是由于安装程序没有启动成功，建议先关机后再启动尝试，注意，千万不要直接重新启动

2、OVA导入后，可能无法联网，请重启系统或在右上角操作重新连接网络（Wired Connected - Turn Off -> connect）

3、首次进入安装界面以及安装后首次登录系统，会有较长的黑屏等待时间，这是因为要启动的服务较多，属于正常现象

# 最后

感谢大家的使用，如有问题请在issus反馈，我们会关注每一个问题并在下一个版本中尝试加以改进，再次感谢。
