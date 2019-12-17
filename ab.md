# ab

Apache HTTP Server benchmarking tool

[Back](README.md) to Linux CheatSheets by Ireaneus

## Send 100 requests with a concurency of 50 requests to an URL

```bash
[user@server1] ab -n 100 -c 50 http://www.example.com/
```

## Send requests during 30 seconds with a concurency of 50 requests to an URL

```bash
[user@server1] ab -t 30 -c 50 URL http://www.example.com/
```
