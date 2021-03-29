# Performance

```
$ sudo nvpmodel -m 0
$ sudo jetson_clocks
```

MAXN 10W mode (default) - persists after restart

```
$ sudo nvpmodel -m 0
```

5W mode

```
$ sudo nvpmodel -m 1
```

maximize platform performance

```
$ sudo jetson_clocks
$ sudo jetson_clocks --show
```

# Sources

- [Supported Modes and Power Efficiency](https://docs.nvidia.com/jetson/l4t/index.html#page/Tegra%20Linux%20Driver%20Package%20Development%20Guide/power_management_nano.html#wwpID0E0FL0HA)
- [Maximizing Jetson Nano ... Performance](https://docs.nvidia.com/jetson/l4t/index.html#page/Tegra%20Linux%20Driver%20Package%20Development%20Guide/power_management_nano.html#wwpID0E0ZB0HA)
- [Chromium browser real-time video on Jetson Nano](https://forums.developer.nvidia.com/t/chromium-browser-real-time-video-on-jetson-nano/126510) - chromium flags for performance
