# English | [简体中文](./README-zh_CN.md)

# TranSec OS
TranSec OS is a car networking penetration testing distribution system based on Ubuntu 18.04, mainly used for security assessment of car networking devices. The system is equipped with hundreds of dedicated testing tools for vehicle networking security, aiming to solve a series of problems for vehicle networking security practitioners, such as messy testing tools, complex testing environment configuration, and no available tools

## Advantages
An out of the box testing environment that includes hundreds of commonly used toolsets for penetration testing of the Internet of Vehicles. Covering security tests such as reverse engineering, CAN, in car Ethernet, WiFi, Bluetooth, cloud platforms, etc
- Permanent free update support, and gradually increasing the targeted free trial of Anheng's self-developed vehicle networking tools and some commercial software in the future
- An open operating environment that allows users to customize and modify any file or install any program within the system
- Built in various commonly used tools under different architectures such as ARM, X86, MIPS, etc., such as adb, gdb, nmap, busybox, etc
- ...

## Tool List (Partial)
Below are some of the tools listed, and more tools can be explored by yourself.
|Tool Name | Tool Introduction|
|--- | ---|
|CANToolz | CAN Analysis Framework|
|Can Utils | Can's testing toolkit|
|Scapy | Packet Processing Tool|
|Proxmark3 | PM3 client|
|Logic | Logic analyzer client|
|URH | Radio Analysis Tools|
|MQTTclient | MQTT client|
|Gattool | BLE Connection Tool|
|Binwalk | Firmware unpacking and analysis tool|
|IDA Free | Professional binary analysis tool|
|Shambles | Professional binary analysis and vulnerability scanning tool, including automatic unpacking and simulation|
|Ghidra | Open source binary analysis tool|
|Jeb | Android Reverse Analysis Tool|
|Jadx Gui | Open source Android reverse analysis tool|
|Hcitool | Bluetooth Connection Tool|
|Ubertool tools | A software and hardware open-source Bluetooth packet catcher|
|Pybluez2 | Python library - Bluetooth attack tool|
|KillerBee | Security research tool for ZigBee|
|HackRF | HackRF supporting software|
|Frida | hook tool|
|Gdb multiarch | Heterogeneous architecture gdb analysis tool|
|Pwndbg | gdb Advanced Script|
|Pwntools | Python vulnerability exploitation framework|
|QEMU | Open Source Simulator|
|Qemu system | Virtual System Simulator|
|Firmware Mod Kit | Firmware Modification Kit|
|Firmware Analysis Toolkit | An open-source firmware analysis tool|
|Frp | Internal network penetration tool|
|MobSF | Android Automated Static Analysis Tool|
|Burpsuite | Web testing tool|
# Download
- GitHub：[Releases](https://github.com/TianWen-Lab/TranSec/releases)
- Baidu Netdisk：[https://pan.baidu.com/s/1jWFxiawgiC57gLCYiSvnyA](https://pan.baidu.com/s/1jWFxiawgiC57gLCYiSvnyA) password:r4x7

# Installation instructions

This system provides ISO image installation and OVA image import installation methods. It is recommended to use OVA to import virtual machines for simpler and more convenient operations. Due to the large size of the system, importing or installing requires a certain amount of time, which depends on the performance of the disk.

After successful import or installation, boot up and use `iov/root` to log in. After successful login, the user experience plan will be displayed, and you can choose to agree or refuse. Once confirmed, you can start using it.

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/8b3dacaf-7668-4be8-baf4-8c4ebdc3fcaa)

## OVA import
Open the OVA file using virtual machine software:

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/168420ab-1064-4452-b201-2d67c5b1ae4a)

## ISO installation
When installing using ISO images, **it is recommended to configure 50GB of disk and 4GB of memory**. After loading the image, select 'Boot system install' to enter the installation process:

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/f51c53c6-bcb1-4d1f-8544-ca87d8f82ac2)

Enter the password `iov/root` to log in to the installation interface:

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/0c76f57a-528f-4226-a744-fca508b2ed7b)

Enter account password and other information according to the prompts, and click Next to enter the partition process:

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/7da9584d-ef52-4b72-93cd-2bdf70803eee)

After selecting the disk, click Delete to delete the partition:

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/e45d4c52-ffe8-43ba-ae1a-709dfb339ccf)

At this point, a `/dev/sda?` will appear, Select `/dev/sda?`, Click on the arrow

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/44e08672-3419-407b-9aaf-6c81442d6213)

At this point, `/dev/sda`  becomes '/dev/sda1 '. Select this partition, select the mounted directory (/) and partition format (ext4) from the drop-down menu on the right, and click the arrow again to complete the partition:

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/e2c4dd07-ba00-43a3-afe3-c3a1fbfef60f)


Returning to the installation process, after checking the box containing user configuration and data (**must be changed to √**), proceed to the next step to proceed with the installation

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/9e4a1ae3-65a1-44f0-8a11-1bfed3d1bb07)

The installation time is about 6 minutes. After the progress is completed, click reboot to complete the installation process and enter the system (If you have other things to do, you can do them first. After the system installation is completed, it will automatically restart after 30 seconds ^o^)

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/57042e75-32c0-4cba-b98a-b92dd730aa36)



# System screenshot
![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/e6d0e230-e90a-48ce-ad69-bb512408c5c7)

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/b564d4f6-18c2-4298-994a-b06d19d2b6b5)

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/a5db4f60-97ff-4c8e-afe4-8437a22e73df)

![image](https://github.com/TianWen-Lab/TranSec/assets/45167857/997e4687-0234-4334-a3b8-ff91ef20539e)

# Possible installation issues
Due to being based on the `systemback`, there may be some issues during system installation. Below are the corresponding solutions:

1. When using the ISO installation method, when logging into the installation interface, the prompt "Cannot start the Systemback graphical user interface! Unable to connect to the X server" or other reasons for not entering the installation interface may be due to the installation program not starting successfully. It is recommended to shut down the computer first and then try installing again. Please be careful not to restart directly.

2. After importing OVA, it may not be possible to connect to the network. Please restart the system or reconnect to the network in the upper right corner (Wired Connected - Turn Off ->connect).

3. When entering the installation interface or first time and logging into the system for the first time after installation, there will be a long black screen waiting time. This is because there are many services to start, which is a normal phenomenon

# Finally
Thank you for your use. If you have any questions, please provide feedback on ISSUS. We will pay attention to each issue and try to improve it in the next version. Thank you again.


