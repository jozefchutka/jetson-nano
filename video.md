# Video

## Play file

With GPU decoding:

```
$ gst-launch-1.0 uridecodebin uri=file:///home/jozef/Desktop/Jellyfish_1080_10s_20MB.mp4 ! nvvidconv ! 'video/x-raw(memory:NVMM),width=1920,height=1080' ! nvoverlaysink
```

## Decoding

- H.264 (3840 x 2160 @60 fps, Up to 120 Mbps)
- H.265 (3840 x 2160 @60 fps, Up to 160 Mbps)
- JPEG (600 MP/sec)
- VP8 (3840 x 2160 @60 fps, Up to 140 Mbps)
- VP9 (3840 x 2160 @60 fps, Up to 120 Mbps)
- MPEG4 (1920×1080 @240 fps, Up to 120 Mbps)

### Concurrency

- 2x H.264 4K @ 30 (YUV 4:2:0)	
- 8x H.264 1080 @ 30 (YUV 4:2:0)
- 2x H.265 4K @ 30 (YUV 4:2:0)
- 8x H.265 1080 @ 30 (YUV 4:2:0)

## Encoding

- H.264 (3840×2160 @30 fps, Up to 120 Mbps)
- JPEG (600 MP/sec)
- H.265 (3840×2160 @30 fps, Up to 100 Mbps)
- VP8 (3840×2160 @30 fps, Up to 120 Mbps)

### Concurrency

- 1x H.264 4K @ 30 (YUV 4:2:0)	
- 4x H.264 1080 @ 30 (YUV 4:2:0)	
- 1x H.265 4K @ 30 (YUV 4:2:0)	
- 4x H.265 1080 @ 30 (YUV 4:2:0)

# Sources

- [Video Decoders](https://docs.nvidia.com/jetson/l4t/index.html#page/Tegra%20Linux%20Driver%20Package%20Development%20Guide/software_features_jetson_nano.html#wwpID0EZHA0) - decoding capabilities
- [Video Encoders](https://docs.nvidia.com/jetson/l4t/index.html#page/Tegra%20Linux%20Driver%20Package%20Development%20Guide/software_features_jetson_nano.html#wwpID0EXHA) - encoding capabilities
- [NVIDIA Video Encode and Decode GPU Support Matrix](https://developer.nvidia.com/video-encode-and-decode-gpu-support-matrix-new)
- [H.264/H.265 Video Encoding Support Matrix for Nvidia Jetson](https://www.stereolabs.com/blog/h-264-h-265-video-encoding-support-matrix-for-nvidia-jetson/)
