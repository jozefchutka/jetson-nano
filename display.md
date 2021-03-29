# Display

## Xorg

Start X server (returns PID):
```
& X :3 -wr > /dev/null 2>&1 &
```

Picks available DISPLAY and returns into stdout:
```
$ X -displayfd /dev/stdout -quiet
```

List runing:
```
$ ps -aux | grep Xorg
```

Kill:
```
$ kill -9 8147
```

Get resolution:
```
$ DISPLAY=:3 xdpyinfo | grep dimensions:
```

Set resolution:
```
$ DISPLAY=:3 xrandr --fb 1920x1080
```

Start app:
```
$ DISPLAY=:3 chromium-browser > /dev/null 2>&1 &
$ DISPLAY=:3 gst-launch-1.0 ximagesrc ! nvvidconv ! fakesink
$ DISPLAY=:3 gnome-calculator
```

## xrandr
```
$ xrandr --listmonitors
```

## Xvfb

Install:
```
$ sudo apt install mesa-utils
$ cd /usr/lib/aarch64-linux-gnu
$ sudo ln -sf libdrm.so.2.4.0 libdrm.so.2
```

Create:
```
$ Xvfb :1 -screen 0 640x480x16
```

List running:
```
$ pidof /usr/bin/Xvfb
```

Make screenshot:
```
$ DISPLAY=:1 import -window root ~/Desktop/screenshot.png
```

Start app:
```
$ DISPLAY=:1 chromium-browser --user-data-dir=~/Desktop/tmp
```
