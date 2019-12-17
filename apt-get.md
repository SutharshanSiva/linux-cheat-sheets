# apt-get

Desc: Allows to update the operating system

[Back](README.md) to README.md

### To fetch package list

```bash
[user@server1]$ apt-get update
```

### To download and install updates without installing new package

```bash
[user@server1]$ apt-get upgrade
```

### To download and install the updates AND install new necessary packages

```bash
[user@server1]$ apt-get dist-upgrade
```

### Full command

```bash
[user@server1]$ apt-get update && apt-get dist-upgrade
```

### To install a new package(s)

```bash
[user@server1]$ apt-get install package(s)
```

#### Download a package without installing it. (The package will be downloaded in your current working dir)

```bash
[user@server1]$ apt-get download modsecurity-crs
```

#### Change Cache dir and archive dir (where .deb are stored)

```bash
[user@server1]$ apt-get -o Dir::Cache="/path/to/destination/dir/" -o Dir::Cache::archives="./" install ...
```

#### Show apt-get installed packages

```bash
[user@server1]$ grep 'install ' /var/log/dpkg.log
```
