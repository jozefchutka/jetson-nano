# Firewall

Check Open Ports:
```
sudo netstat -tulpn | grep LISTEN
sudo ss -tulpn
```

Open Port:
```
sudo iptables -A INPUT -p tcp --dport 8080 -j ACCEPT
sudo iptables-save
```
