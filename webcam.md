# Webcam

Webcam info:
```
$ v4l2-ctl --all
$ v4l2-ctl -V
```

Available formats:
```
$ v4l2-ctl --list-formats-ext -d /dev/video0
```

change default format(?):
```
$ v4l2-ctl -d /dev/video0 --set-fmt-video=width=640,height=480,pixelformat=JPEG
```

## GStreamer

Microsoft Lifecam VX 1000:
```
$ gst-launch-1.0 v4l2src ! jpegdec ! xvimagesink
```

## Droidcam / IP Webcam

Install [DroidCam](https://play.google.com/store/apps/details?id=com.dev47apps.droidcam&hl=en&gl=US) on Android phone and read frames with:

```
cv2.VideoCapture("http://192.168.2.101:4747/mjpegfeed")
```

