## conky
<img src='a.png' width='900px'>
<img src='b.png' width='900px'>

## 第一次制作conky，工程框架取自：  
- https://github.com/alexbel/conky.git
## 修改成了自己喜欢的风格和模块。  

## 下载：  
- `git clone https://github.com/caiyufeng/conky.git  ~/.conky`

## 修改secrets.yml里面的分区路径，用于file模块显示内存占比  
- `gedit ~/.conky/secrets.yml`

## 修改file.conf里面的note文件路径，用于file模块显示文件内容  
- `gedit ~/.conky/configs/file.conf`

## 安装ruby和conky  
- `sudo apt-get install ruby`
- `sudo apt-get install conky`

## 安装依赖  
- curl
- ss
- acpi
- sensors

## 我的电脑只需要安装sensors：  
- `sudo apt-get install lm-sensors`
- `sudo sensors-detect `
- `service module-init-tools start`

## 开机自启动：
Create a file `conky.desktop` in `~/.config/autostart` directory and fill it in with the following contents:  
```
[Desktop Entry]
Name=conky
Exec=cd ~/.conky && ruby starter.rb
Type=Application
Terminal=false
```

## 重启脚本：  
```
#! /bin/bash
sudo killall $"conky"
cd ~/.conky/
./starter.rb
```
## 无法挂载Windows的盘(例如sda8)：  
- sudo ntfsfix /dev/sda8

## 更多问题请移步至原作主页  
