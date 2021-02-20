# Virtual Display Linux (VDL Monitor)

Just a simple bash script that create some virtual display / monitor on linux OS for extended display via *TeamViewer* or *VNC server*

Yes, you can add fake display monitor without real monitor attached!

![Virtual Monitor Linux](https://raw.githubusercontent.com/dianariyanto/virtual-display-linux/master/Screenshot2.png)

![Virtual Display Linux (VDL Monitor)](https://raw.githubusercontent.com/dianariyanto/virtual-display-linux/master/Screenshot.png)

I'm using this simple script for extend my desktop pc to "2 external monitor" via teamviewer.

# Quick Setup

1. Install teamviewer on both devices. (You also can use VNC to)
2. `cd ~`
3. `git clone https://github.com/dianariyanto/virtual-display-linux.git`
4. `cd virtual-display-linux`
6. `sudo chmod +x vdl-monitor`
5. Change your own resolution setup `vdl-monitor.conf`
6. `./vdl-monitor`
7. For first running, you will prompt to reboot or relogin current session
8. `cd ~/virtual-display-linux/`
9. `./vdl-monitor`
10. Done.

```shell
dianariyanto@lenovo:~$ cd virtual-display-linux/
dianariyanto@lenovo:~/virtual-display-linux$ ./vdl-monitor 
Start configuration
add resolution 1368x768
start display VIRTUAL1 to 1368x768
Screen 0: minimum 8 x 8, current 2968 x 900, maximum 32767 x 32767
LVDS1 connected primary 1600x900+1368+0 (normal left inverted right x axis y axis) 310mm x 170mm
   1600x900      60.00*+  59.82  
   1400x900      59.88  
   1368x768      60.00    59.88    59.85  
   1360x768      59.80    59.96  
   1280x800      59.81    59.91  
   1152x864      60.00  
   1280x720      59.86    60.00    59.74  
   1024x768      60.00  
   1024x576      60.00    59.90    59.82  
   960x540       60.00    59.63    59.82  
   800x600       60.32    56.25  
   864x486       60.00    59.92    59.57  
   800x450       60.00  
   640x480       59.94  
   720x405       59.51    60.00    58.99  
   640x360       59.84    59.32    60.00  
DP1 disconnected (normal left inverted right x axis y axis)
DP2 disconnected (normal left inverted right x axis y axis)
DP3 disconnected (normal left inverted right x axis y axis)
HDMI1 disconnected (normal left inverted right x axis y axis)
HDMI2 disconnected (normal left inverted right x axis y axis)
HDMI3 disconnected (normal left inverted right x axis y axis)
VGA1 disconnected (normal left inverted right x axis y axis)
VIRTUAL1 connected 1368x768+0+0 (normal left inverted right x axis y axis) 0mm x 0mm
   1368x768      60.00* 
VIRTUAL2 disconnected (normal left inverted right x axis y axis)

Done, Check your VDL Monitor on System Setting > Display
dianariyanto@lenovo:~/virtual-display-linux$ 

```

Check teamviewer client and select your virtual display act as external monitor.

You now success Add Fake Display with No Monitor is Plugged In!

## Confirmed

* Elementary OS 5.0 Juno based on Ubuntu 18.04 with *Teamviewer v.14.7.19.65*
* Pop OS! 20.04 Default Share Screen with Remmina Desktop Client
* Armbian 5.0 xrdp with Realvnc Client
* Waiting your report here.

## Not working on Nvidia GPU
you need to adjust the configuration according to the graphics card you are using

Default xorg config for intel

File : 20-intel.conf
```
Section "Device"
    Identifier "intelgpu0"
    Driver "intel"
    Option "VirtualHeads" "2"
EndSection
```
need further confirmation if you can modify the configuration against other graphics cards. 


https://github.com/dianariyanto/virtual-display-linux/issues/9 (not supported xorg config)

## Remote Client

https://www.teamviewer.com/en/download/linux/
https://www.realvnc.com/en/connect/download/viewer/
https://remmina.org/
