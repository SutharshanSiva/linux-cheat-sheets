# apt-cache

[Back](README.md) to Linux CheatSheets by Ireaneus

### To search for apt packages

```bash
[user@server1]$ apt-cache search "whatever"
```

### To display package records for the named package(s)

```bash
[user@server1]$ apt-cache show pkg(s)
```

### To display reverse dependencies of a package

```bash
[user@server1]$ apt-cache rdepends package_name
```

### To display package versions, reverse dependencies and forward dependencies of a package

```bash
[user@server1]$ apt-cache showpkg package_name
```
