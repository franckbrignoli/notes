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

### Grep Multiple Values 

```text
$ grep -f file_pattern.txt file.txt
```

### Generate QR Code for WIFI

```text
$ brew install qrencode
$ qrencode -o wifi.png "WIFI:T:WPA;S:<SSID>;P:<PASSWORD>;;"
```

### Images To SVG

\(thanks to [arkwrite](https://twitter.com/arkwrite/status/1212082448567349248?s=20)\)

```text
$ brew install imagemagick potrace 
$ convert $filename.png -type Grayscale -scale "100%" -auto-gamma -auto-level -brightness-contrast 40x40 $filename.bmp
$ potrace -s -H 400pt -t 10 -z black -C "#444444" --tight $filename.bmp
```

### Varnish

Backend health

```text
$ varnishadm debug.health
```

Backend list

```text
$ varnishadm backend.list
```

