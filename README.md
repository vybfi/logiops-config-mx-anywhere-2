# logiops-config-mx-anywhere-2
MX Anywhere 2 的 logiops 配置文件
logipos用于在linux下自定义鼠标按键功能
本配置文件fork自vgocoder
在其基础上关闭了鼠标中键手势的向左和向右
并将鼠标滚轮左滚和右滚设置为复制和粘贴.
(同时进行了一部分汉化)

## 使用方法
### 安装 logiops
```shell
# Ubuntu Or Debian
sudo apt-get install logiops
# Arch Linux
sudo pacman -S logiops
```
> 笔者没有确定是否可以直接apt安装, 我是直接根据原github库的指引编译安装

### 配置 logiops
拉取本项目文件并将配置文件copy到指定位置
```shell
git clone https://github.com/vybfi/logiops-config-mx-anywhere-2.git
cd logiops-config-mx-anywhere-2
cp logid.cfg /etc/logid.cfg
```
### 启动 logiops
```shell
sudo systemctl start logid
```
### 停止 logiops
```shell
sudo systemctl stop logid
```
### 检查 logiops 状态
```shell
sudo systemctl status logid
```
### 重启 logiops
```shell
sudo systemctl restart logid
```
### 启动 logiops 的debug模式
```shell
sudo logid -v
```
### 卸载 logiops
```shell
# Ubuntu Or Debian
sudo apt-get remove logiops
# Arch Linux
sudo pacman -R logiops
```

### 开机自启动
```shell
sudo systemctl enable --now logid
```

## CIDs列表

    0x50 (鼠标左键)
    0x51 (鼠标右键)
    0x52 (鼠标中键)
    0x53 (鼠标侧键-向后)
    0x56 (鼠标侧键-向前)
    0x5b (左滚动)
    0x5d (右滚动)
    0xd7 (Switch Receivers)


## Thanks
[PixlOne/logiops](https://github.com/PixlOne/logiops)

[vgocoder/logiops-config-mx-anywhere-2](https://github.com/vgocoder/logiops-config-mx-anywhere-2)
