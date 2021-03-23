Disable GUI on boot:
```
$ sudo systemctl set-default multi-user.target
```

Enable GUI on boot:
```
$ sudo systemctl set-default graphical.target
```

Start GUI session:
```
$ sudo systemctl start gdm3.service
```

- [How to boot Jetson Nano in text mode?](https://forums.developer.nvidia.com/t/how-to-boot-jetson-nano-in-text-mode/73636/11)
