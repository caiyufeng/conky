## Cooler Conky
<img src='a.png' width='900px'>
<img src='b.png' width='900px'>

## Recreate
- https://github.com/alexbel/conky.git  

## Download
- `git clone https://github.com/caiyufeng/conky.git  ~/.conky`  

## Modify
put your path in it
- `gedit ~/.conky/secrets.yml`
- `gedit ~/.conky/configs/file.conf`  

## Install
ruby & conky
- `sudo apt-get install ruby`
- `sudo apt-get install conky`  
sensors:
- `sudo apt-get install lm-sensors`
- `sudo sensors-detect `
- `service module-init-tools start`  
other dependencies:
- curl
- ss
- acpi
- conky-imlib2  

## Autostart：
- `cd ~/.config/autostart`
- `gedit conky.desktop`  
```
[Desktop Entry]
Name=conky
Exec=cd ~/.conky && ruby starter.rb
Type=Application
Terminal=false
```  

## Restart
```
#! /bin/bash
sudo killall $"conky"
cd ~/.conky/
./starter.rb
```  
## Error mounting sda8：  
- sudo ntfsfix /dev/sda8  

## More questions please move to the original author homepage
