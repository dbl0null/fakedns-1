# fakedns

> Fake DNS server written in python 2

## What it does?

It responds to DNS `A` questions (host address questions), responding with the same IP over and over. The server is intended to be used when testing HTTP crawlers.

## Usage

```
$ python fakedns.py --help
usage: fakedns.py [-h] [--host HOST] [--port PORT] [--reply REPLY]

Fake DNS server

optional arguments:
  -h, --help     show this help message and exit
  --host HOST    listen host
  --port PORT    listen port
  --reply REPLY  ipaddr to reply
```


```shell
$ python fakedns.py --port 1024
```

```shell
$ nslookup -port 1024  www.baidu.com  0.0.0.0
Server:         0.0.0.0
Address:        0.0.0.0#1024

Non-authoritative answer:
Name:   www.baidu.com
Address: 0.0.0.0
```

## License

Copyright (c) 2014 Patryk Hes. Licensed under MIT license.
