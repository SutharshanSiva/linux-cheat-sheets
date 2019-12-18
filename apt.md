# apt

[Back](README.md) to Linux CheatSheets by Ireaneus

### To search a package

```bash
[user@server1]$ apt search package
```

### To show package informations

```bash
[user@server1]$ apt show package
```

### To fetch package list

```bash
[user@server1]$ sudo apt update
```

### To download and install updates without installing new package

```bash
[user@server1]$ sudo apt upgrade
```

### To download and install the updates AND install new necessary packages

```bash
[user@server1]$ sudo apt dist-upgrade
```

### Full command

```bash
[user@server1]$ sudo apt update && apt dist-upgrade
```

### To install a new package(s)

```bash
[user@server1]$ sudo apt install package(s)
```

### To uninstall package(s)

```bash
[user@server1]$ sudo apt remove package(s)
```
