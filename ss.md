# ss - Utility to investigate sockets
[Back](README.md) to README.md

## Args
-4/-6 list ipv4/ipv6 sockets
-n numeric addresses instead of hostnames
-l list listing sockets
-u/-t/-x list udp/tcp/unix sockets
-p Show process(es) that using socket

## show all listing tcp sockets including the corresponding process
```sh
ss -tlp
```

## show all sockets connecting to 192.168.2.1 on port 80
```sh
ss -t dst 192.168.2.1:80
```

## show all ssh related connection
```sh
ss -t state established '( dport = :ssh or sport = :ssh )'
```

## List all the tcp sockets in state FIN-WAIT-1 for our apache to network 193.233.7/24 and look at their timers.
```sh
ss -o state fin-wait-1 '( sport = :http or sport = :https )' dst 193.233.7/24
```

## Display all TCP sockets with process SELinux security contexts.
```sh
ss -t -a -Z
```
