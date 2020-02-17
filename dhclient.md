# dhclient - dhcp client utility

[Back](README.md) to Linux CheatSheets by Ireaneus

To release the current IP address:

```bash
[root@server1] sudo dhclient -r
```

To obtain a new IP address:

```bash
[root@server1] sudo dhclient
```

*Running the above in sequence is a common way of refreshing an IP.*

To obtain a new IP address for a specific interface:

```bash
[root@server1] sudo dhclient eth0
```
