# df - disk free

[Back](README.md) to Linux CheatSheets by Ireaneus

Printout disk free space in a human readable format

```bash
[root@server1] df -h
```

To see FS type

```bash
[root@server1] df -Th
```

Number of files search

```bash
[root@server1] echo "Detailed Inode usage for: $(pwd)" ; for d in `find -maxdepth 1 -type d |cut -d\/ -f2 |grep -xv . |sort`; do c=$(find $d |wc -l) ; printf "$c\t\t- $d\n" ; done ; printf "Total: \t\t$(find $(pwd) | wc -l)\n"

[root@server1] find . -printf "%h\n" | cut -d/ -f-2 | sort | uniq -c | sort -rn

[root@server1] find / -xdev -printf '%h\n' | sort | uniq -c | sort -k 1 -n
```
