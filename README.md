# Arduino IDE on UBUNTU
## Install and setup arduino IDE on ubuntu

1. __Download the newest version of Arduino IDE__ at https://www.arduino.cc/en/software and choose .AppImage for linux
2. Open terminal and __go to .AppImage file's directory__
```
cd Downloads
```
3. Give execution access to .AppImage
```
chmod +x arduino-ide_*.AppImage
```
4. __Run Arduino IDE__
```
./arduino-ide_*.AppImage --no-sandbox
```

## Solved ERROR
### AppImages require FUSE to run. 
*You might still be able to extract the contents of this AppImage 
if you run it with the --appimage-extract option. 
See https://github.com/AppImage/AppImageKit/wiki/FUSE 
for more information*

__Install Libfuse2__
```
sudo apt update
sudo apt install libfuse2 -y
```
### Sandbox Error
*r: 0
License accepted
[11323:0315/165559.773244:FATAL:setuid_sandbox_host.cc(158)] The SUID sandbox helper binary was found, but is not configured correctly. Rather than run without sandboxing I'm aborting now. You need to make sure that /tmp/.mount_arduinpEQrIt/chrome-sandbox is owned by root and has mode 4755.
Trace/breakpoint trap (core dumped)*

__Run Arduino IDE with following commands__
```
./arduino-ide_*.AppImage --no-sandbox
```

## Permanent alias to run Arduino IDE
__run the following command__
```
nano ~/.bashrc
```
__add this on the bottom__
```
alias arduino-ide='/home/user/moses-jaguar/arduino-ide_*.AppImage --no-sandbox'
```
pay attention on *'./arduino-ide_*.AppImage --no-sandbox' and the path*

__last__
```
source ~/.bashrc
```


## Run Arduino IDE
```
arduino
```

# Install STM32duino (Arduino Core for STM32)
1. Buka Arduino IDE
2. Pergi ke File → Preferences
3. Tambahkan URL berikut di Additional Board Manager URLs:
```
https://github.com/stm32duino/BoardManagerFiles/raw/main/package_stmicroelectronics_index.json
```
4. Install "STM32 MCU based boards" by STM32duino pada Board Manager
5. Install STLINK Driver dari STMicroelectronics
```
https://www.st.com/en/development-tools/stsw-link007.html
```
6. Download STM32CubeProgrammer
```
https://www.st.com/en/development-tools/stm32cubeprog.html
```





