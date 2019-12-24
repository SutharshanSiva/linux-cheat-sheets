# cp

[Back](README.md) to Linux Cheatsheets by Ireaneus

To copy a file only if it is newer than last backup

```bash
[user@server1]$ cp -u ~/file1 ~/backup
```

To copy a directory and files

```bash
[user@server1]$ cp -R
[user@server1]$ cp -r
[user@server1]$ cp --recursive
```

To force a copy

```bash
[user@server1]$ cp -f
[user@server1]$ cp --force
```

To preserve a file's attributes

```bash
[user@server1]$ cp -p
```

To copy a single file to multiple files:

```bash
[user@server1]$ cat host1 | tee host2 host3
```
