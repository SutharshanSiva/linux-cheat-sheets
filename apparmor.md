# apparmor

Desc: Apparmor will protect the system by confining programs to a limited set of resources.

[Back](README.md) to Linux CheatSheets by Ireaneus

### To activate a profile

```bash
[user@server1]$ sudo aa-enforce usr.bin.firefox
# OR
[user@server1]$ export _PROFILE_='usr.bin.firefox' sudo $(rm /etc/apparmor.d/disable/$_PROFILE_ ; cat /etc/apparmor.d/$_PROFILE_ | apparmor_parser -a )
```

### TO disable a profile

```bash
[user@server1]$ sudo aa-disable usr.bin.firefox
# OR
[user@server1]$ export _PROFILE_='usr.bin.firefox' sudo $(ln -s /etc/apparmor.d/$_PROFILE_ /etc/apparmor.d/disable/ && apparmor_parser -R /etc/apparmor.d/$_PROFILE_)
```

### To list profiles loaded

```bash
[user@server1]$ sudo aa-status
# OR
[user@server1]$ sudo apparmor_status
```

### List of profiles available

```bash
[user@server1]$ ls -l /etc/apparmor.d/
```
