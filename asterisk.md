# asterisk

[Back](README.md) to Linux CheatSheets by Ireaneus

### To connect to a running Asterisk session

```bash
[user@server1]$ asterisk -rvvv
```

### To issue a command to Asterisk from the shell

```bash
[user@server1]$ asterisk -rx "<command>"
```

### To originate an echo call from a SIP trunk on an Asterisk server, to a specified number

```bash
[user@server1]$ asterisk -rx "channel originate SIP/<trunk>/<number> application echo"
```

### To print out the details of SIP accounts

```bash
[user@server1]$ asterisk -rx "sip show peers"
```

### To print out the passwords of SIP accounts

```bash
[user@server1]$ asterisk -rx "sip show users"
```

### To print out the current active channels

```bash
[user@server1]$ asterisk -rx "core show channels"
```
