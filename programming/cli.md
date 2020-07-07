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

### Grep

```text
# search for multiple values contained in a file 
$ grep -f file_pattern.txt file.txt

# display filename only
$ grep -l 
```

#### 

### Generate QR Code for WIFI

```text
$ brew install qrencode
$ qrencode -o wifi.png "WIFI:T:WPA;S:<SSID>;P:<PASSWORD>;;"
```

\(or [browser version](https://qifi.org/)\)

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

### JQ 

* [https://mosermichael.github.io/jq-illustrated/dir/content.html](https://mosermichael.github.io/jq-illustrated/dir/content.html)

Existing key

```text
$ cat stuff.json | jq ".[] | select(.clientNumber != null)"
```

### Curl

Display requests timings \(from [stackoverflow](https://stackoverflow.com/a/22625150)\)

```text
$ cat curl-format.txt
    time_namelookup:  %{time_namelookup}s\n
       time_connect:  %{time_connect}s\n
    time_appconnect:  %{time_appconnect}s\n
   time_pretransfer:  %{time_pretransfer}s\n
      time_redirect:  %{time_redirect}s\n
 time_starttransfer:  %{time_starttransfer}s\n
                    ----------\n
         time_total:  %{time_total}s\n
         
$ curl http://google.com -w "@curl-format.txt"
```

### Templating

```text
FOO=foo
BAR=bar
export FOO BAR

envsubst <<EOF
FOO is $FOO
BAR is $BAR
EOF
```

### Sort

```text
sort sum.txt --key 1,2 --stable
```

`--key` uses only the specified fields for sorting

`--stable`

