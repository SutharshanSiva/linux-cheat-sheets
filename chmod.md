# chmod

[Back](README.md) to Linux Cheatsheets by Ireaneus

#### Add execute for all (myscript.sh)

```bash
[user@server1]$ chmod a+x myscript.sh
```

#### Set user to read/write/execute, group/global to read only (myscript.sh), symbolic mode

```bash
[user@server1]$ chmod u=rwx, go=r myscript.sh
```

#### Remove write from user/group/global (myscript.sh), symbolic mode

```bash
[user@server1]$ chmod a-w myscript.sh
```

#### Remove read/write/execute from user/group/global (myscript.sh), symbolic mode

```bash
[user@server1]$ chmod = myscript.sh
```

#### Set user to read/write and group/global read (myscript.sh), octal notation

```bash
[user@server1]$ chmod 644 myscript.sh
```

#### Set user to read/write/execute and group/global read/execute (myscript.sh), octal notation

```bash
[user@server1]$ chmod 755 myscript.sh
```

#### Set user/group/global to read/write (myscript.sh), octal notation

```bash
[user@server1]$ chmod 666 myscript.sh
```

#### Set permissions on a directory

```bash
[user@server1]$ chmod 755 /opt/myapp
```

#### Set permissions on a directory and files recursivley

```bash
[user@server1]$ chmod 666 -R /opt/myapp/*
```

### Roles

| role | description |
| --- | --- |
| u | user (owner of the file) |
| g | group (members of file's group) |
| o | global (all users who are not owner and not part of group) |
| a | all (all 3 roles above) |
| | |

### Numeric representations

| numeric | description |
| --- | --- |
| 7 | full (rwx) |
| 6 | read and write (rw-) |
| 5 | read and execute (r-x) |
| 4 | read only (r--) |
| 3 | write and execute (-wx) |
| 2 | write only (-w-) |
| 1 | execute only (--x) |
| 0 | none (---) |
| | |