# Virtual Display Linux (VDL Monitor)

Just a simple bash script that create some virtual display / monitor on linux OS for extended display via *TeamViewer* or *VNC server*

![Virtual Monitor Linux](https://raw.githubusercontent.com/dianariyanto/virtual-display-linux/master/Screenshot2.png)

![Virtual Display Linux (VDL Monitor)](https://raw.githubusercontent.com/dianariyanto/virtual-display-linux/master/Screenshot.png)

I'm using this simple script for extend my desktop pc to "2 external monitor" via teamviewer.

# Quick Setup

Tested on Elementary OS 5.0 Juno based on Ubuntu 18.04 with *Teamviewer v.14.7.19.65*

1. Install teamviewer on both devices. (You also can use VNC to)
2. `cd ~`
3. `git clone https://github.com/dianariyanto/virtual-display-linux.git`
4. `cd virtual-display-linux`
5. Change your own resolution setup `vi vdl-monitor.conf`
6. `sudo bash vdl-monitor`
7. Logout from current session then login again
8. `cd ~/virtual-display-linux/`
9. `bash vdl-monitor`
10. Done.

Now check teamviewer client and select your virtual display act as external monitor.

https://www.teamviewer.com/en/download/linux/