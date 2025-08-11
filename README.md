# intel_i225_i226_firmware
英特尔i225V与i226V网卡固件及升级指南

Version i225 - V1.94 
Version i226 - V2.32


# i225-V
1. 安装驱动
右键iqvsw64e.inf，安装
2. 查看当前固件版本
管理员打开Powershell或者CMD
```cmd
cd 到当前目录
.\EEUPDATEW64e.exe /nic=1 /eepromver
```
3. 更新固件
注意：如果你有多个网卡设备，请先将其他网卡设备在设备管理器中禁用
## 版本 1.94
```cmd
.\EEUPDATEW64e.exe /nic=1 /d NVM\Foxpond1_I225_15F3_V_1MB_1p94.bin
```
4. 关闭电脑，并拔掉电源线（如果你开启了网络唤醒，网卡关机不会断电），等一分钟再开机 ！！非常重要
5. 再次查看版本信息，验证升级
```cmd
.\EEUPDATEW64e.exe /nic=1 /eepromver
```

# i226-V
1. 安装驱动
同样的，右键iqvsw64e.inf，安装
2. 查看当前固件版本
管理员打开Powershell或者CMD
```cmd
cd 到当前目录
.\EEUPDATEW64e.exe /nic=1 /eepromver
```
3. 更新固件
注意：如果你有多个网卡设备，请先将其他网卡设备在设备管理器中禁用
## 版本 2.32 2MB
```cmd
.\EEUPDATEW64e.exe /nic=1 /d NVM\FXVL_125C_V_2MB_2.32.bin
```
## 版本 2.32 1MB
```cmd
.\EEUPDATEW64e.exe /nic=1 /d NVM\FXVL_125C_V_1MB_2.32.bin
```
固件有2MB版本和1MB版本，不知道固件大小是多少没关系，先刷2MB版本，如果你的固件是1MB的话，它会提示`1:  Shared Flash image update FAILED! Flash index is bad or out of range`，此时就换刷1MB固件

4. 关闭电脑，并拔掉电源线（如果你开启了网络唤醒，网卡关机不会断电），等一分钟再开机 ！！非常重要
5. 再次查看版本信息，验证升级
```cmd
.\EEUPDATEW64e.exe /nic=1 /eepromver
```
