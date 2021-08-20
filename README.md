# Hackintosh for DeskMini 110, QNVH(i7-8750H ES), AC3168, using Opencore and Support macOS Big Sur  

![image](https://github.com/dfc643/DeskMini-110-Hackintosh/blob/master/screenshots/finder.png?raw=true)  

---

**使用EFI前请务必修改三码(SSN,UUID,ROM)**    
**Please change three system codes (SSN,UUID,ROM) before using this EFI**   

---

# Thanks/喝水不忘挖井人
* 感谢 @github-wang 提供的 [Hackintosh-Deskmini110-i5-6500-opencore](https://github.com/github-wang/Hackintosh-Deskmini110-i5-6500-opencore) （借鉴70%）
* 感谢 @Road-tech 提供的 [Hackintosh-Asus-H110T-QNVH-I7-8850H-DW1820A-OC](https://github.com/Road-tech/Hackintosh-Asus-H110T-QNVH-I7-8850H-DW1820A-OC) （借鉴20%，含README）

---

# Hardware/硬件
|  | Specifications / 型号 | Note / 备注 |
|-------------------------|:---------------------------------:|:-------------------------------:|
| Motherboard/主板: | ASRock DeskMini 110 | STX |
| CPU/处理器: | QNVH (ES) | i7-8750H (ES) |
| CPU Cooler/散热器: | Cheap AVC Fan | 25块包邮的AVC风扇 |
| Hard Drive/硬盘: | SuperSSpeed 120G SSD (MLC) | 便宜的超极速MLC固态120G |
| RAM/内存: | 8G DDR4 2400MHz ×2 | 海盗船 + 三星 |
| Wireless Card/无线网卡: | Intel Wireless AC 3168 | 35块钱包邮的网卡 |
| Tower Case/机箱: | DeskMini Gen 1 | 华擎 DeskMini 一代 |
| Power/电源: | Acbel 120W DC Adapter | 120瓦直流电源 |
  
---

# Functions/功能
### Work：
- HDMI port (1080p) ｜ HDMI接口
- DP port (1080p) ｜ DP接口
- Audio output on HDMI ｜ HDMI接口音频输出
- All USB ports ｜ 所有USB接口
- Wi-Fi & Bluetooth ｜ Wi-Fi & 蓝牙
- Network Interface Card ｜ 千兆
- 3.5mm Audio Output & Mic Input ｜ 3.5mm音频输出
- hyper-threading ｜ 超线程
- 已加载原生电源管理
- CPU变频
- HEVC硬解码

### Not tested yet:
- Airdrop ｜ 隔空投送（BGA魔改CPU不能用）
- AirPlay ｜ 投屏
- Continuity ｜ 接力   
- 4k display ｜ 4K输出  （我没有4K屏）
- NVME | NVME（我没有）

### Doesn't Work :
- Sleep ｜ 睡眠（会睡死）

---

# EFI files download/EFI 文件下载

- DL LINK | 下载地址: https://github.com/dfc643/DeskMini-110-Hackintosh/releases

### op0.6.9-deskmini110-uhd630-bigsur-es.zip
- use itlwm kext | 使用 itlwm 无线驱动
- need install HeliPort as wifi client | 需要在系统中安装 HeliPort 作为无线客户端
- not support airdrop | 不支持隔空投送
- supports all CPUs | 支持所有 UHD 630 核显的 CPU
- support uhd 630 only | 只支持 UHD 630
- no need intel me | 不需要 Intel ME

### op0.6.9-deskmini110-uhd630-bigsur-AirportItlwm.zip
- use AirportItlwm kext | 使用 AirportItlwm 无线驱动
- support airdrop | 支持隔空投送
- supports SKL,KBL,CFL CPUs | 只支持正式版CPU，不支持ES和转针CPU
- support uhd 630 only | 只支持 UHD 630
- need intel me | 需要 Intel ME
  
---

# Modified BIOS/魔改BIOS

Modified BIOS for CoffeeLake and BGA 1440 CPUs. no need for Skylake and KabyLake CPUs.

魔改 BIOS 只有第 8 代，或者笔记本转针 CPU 才需要，第 6、7 代 CPU 不需要刷。

You need to prepare a device programmer like ch341a, GZU OnePro(Recommend),

**建议使用编程器刷入BIOS！**

当然你也可以尝试软刷BIOS，具体教程和BIOS文件都打包在[deskmini110_cfl_bios_210811.zip](https://github.com/dfc643/DeskMini-110-Hackintosh/raw/main/deskmini110_cfl_bios_210811.zip)

---

# BIOS setting/BIOS设定：

### Disable：
- Fast Boot    
- VT-d  
- CSM  
- Intel SGX 
- Serial Port  

### Enable：
- Intel Virtualization Technology   
- Hyper Threading 
  
---
  
# Install macOS/安装macos

Please look at [Hackintosh-Asus-H110T-QNVH-I7-8850H-DW1820A-OC](https://github.com/Road-tech/Hackintosh-Asus-H110T-QNVH-I7-8850H-DW1820A-OC), thanks to @Road-tech.

请参考 @Road-tech 提供的 [Hackintosh-Asus-H110T-QNVH-I7-8850H-DW1820A-OC](https://github.com/Road-tech/Hackintosh-Asus-H110T-QNVH-I7-8850H-DW1820A-OC) 里面的教程。

---

# Screenshot/系统展示

![image](https://github.com/dfc643/DeskMini-110-Hackintosh/blob/master/screenshots/finder.png?raw=true)  

![image](https://github.com/dfc643/DeskMini-110-Hackintosh/blob/master/screenshots/wifi.png?raw=true)  

![image](https://github.com/dfc643/DeskMini-110-Hackintosh/blob/master/screenshots/bluetooth.png?raw=true)  

---
# Reference/参考

[精解OpenCore](https://blog.daliansky.net/OpenCore-BootLoader.html) - [黑果小兵的部落阁 ](https://blog.daliansky.net/)

[使用OpenCore引导黑苹果](https://blog.xjn819.com/?p=543) - [XJN](https://blog.xjn819.com/) 

[Asrock deskmini 310-com hackintosh 10.14-10.15 EFI](https://blog.xjn819.com/?p=7) - [XJN](https://blog.xjn819.com/)

[DW1820A/BCM94350ZAE/BCM94356ZEPA50DX插入的正确姿势](https://blog.daliansky.net/DW1820A_BCM94350ZAE-driver-inserts-the-correct-posture.html) - [黑果小兵的部落阁](https://blog.daliansky.net/)

[华硕 ASUS H110T 支持 8 代 9 代 Xeon BIOS](http://www.smxdiy.com/thread-1862-1-1.html) - [D大](http://www.smxdiy.com/space-uid-1196.html)
