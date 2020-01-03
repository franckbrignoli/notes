# CLI

### Nmap 

Find devices on your network

```text
$ nmap -sP 192.168.1.1-255
```

### Compare Files

Show the lines in 1 but not in 2 \(-2 hide the ones present only in 2, -3 

```text
$ comm -23 1.txt 2.txt
```

### Generate QR Code for WIFI

```text
$ brew install qrencode
$ qrencode -o wifi.png "WIFI:T:WPA;S:<SSID>;P:<PASSWORD>;;"
```

