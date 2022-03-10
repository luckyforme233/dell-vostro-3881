# 台式机 Dell-Vostro-3881


| 规格     | 详情                   |
| -------- | ---------------------- |
| 电脑型号 | 戴尔成就系列3881       |
| 操作系统 | macOS big sur  (11.5)        |
| 处理器   | I5-10400               |
| 内存     | 16G                    |
| 显卡     | Intel UHD 630 Graphics |
| 网卡     | RTL8111                |
| 声卡     | VoodooHDA万能声卡，目前我使用的蓝牙耳机或者蓝牙音箱|

![image](https://user-images.githubusercontent.com/18027182/126869997-6000d520-f05d-4f57-92a8-5d8a8bc32b46.png)



# OC版本 > 0.7.2

## 那些功能正常

1. CPU睿频
2. 核显解码（DVMT 64M）
3. 风扇控制（isata menus）
4. 板载网卡 + wifi + 蓝牙
5. 休眠
6. USB
7. 万能声卡



# 解锁BIOS步骤
![image](https://user-images.githubusercontent.com/18027182/157573811-91c7df46-6bfc-426f-9007-dd53026d38c3.png)

![image](https://user-images.githubusercontent.com/18027182/157573824-611e5935-9ff8-4e0e-a3cb-b29b30bfbdeb.png)



###  BIOS 设置

#### [#](https://dortania.github.io/OpenCore-Install-Guide/config.plist/coffee-lake.html#disable)Disable

- Fast Boot
- Secure Boot
- Serial/COM Port
- Parallel Port
- VT-d (can be enabled if you set `DisableIoMapper` to YES)
- CSM
- Thunderbolt(For initial install, as Thunderbolt can cause issues if not setup correctly)
- Intel SGX
- Intel Platform Trust
- CFG Lock (MSR 0xE2 write protection)(**This must be off, if you can't find the option then enable both `AppleCpuPmCfgLock` and `AppleXcpmCfgLock` under Kernel -> Quirks. Your hack will not boot with CFG-Lock enabled**)

#### [#](https://dortania.github.io/OpenCore-Install-Guide/config.plist/coffee-lake.html#enable)Enable

- VT-x
- Above 4G decoding
- Hyper-Threading
- Execute Disable Bit
- EHCI/XHCI Hand-off
- OS type: Windows 8.1/10 UEFI Mode
- DVMT Pre-Allocated(iGPU Memory): 64MB
- SATA Mode: AHCI



# 参考连接

https://www.zdynb.cn/2020/jie-suo-cfg-lock.html


https://github.com/HassanElDessouki/DV3888-Hackintosh

