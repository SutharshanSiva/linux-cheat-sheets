# diff

[Back](README.md) to Linux CheatSheets by Ireaneus

To view the differences between two files:

```bash
[root@server1] diff -u version1 version2
```

To view the differences between two directories:

```bash
[root@server1] diff -ur folder1/ folder2/
```

To ignore the white spaces:

```bash
[root@server1] diff -ub version1 version2
```

To ignore the blank lines:

```bash
[root@server1] diff -uB version1 version2
```

To ignore the differences between uppercase and lowercase:

```bash
[root@server1] diff -ui version1 version2
```

To report whether the files differ:

```bash
[root@server1] diff -q version1 version2
```

To report whether the files are identical:

```bash
[root@server1] diff -s version1 version2
```

To diff the output of two commands or scripts:

```bash
[root@server1] diff <(command1) <(command2)
```
