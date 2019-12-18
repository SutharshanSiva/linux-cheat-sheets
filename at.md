# at

[Back](README.md) to Linux CheatSheets by Ireaneus

### To schedule a one time task

```bash
[user@server1]$ at {time}
{command 0}
{command 1}
Ctrl-d
```

### {time} can be either

```bash
[user@server1]$ now | midnight | noon | teatime (4pm)
HH:MM
[user@server1]$ now + N {minutes | hours | days | weeks}
MM/DD/YY
```

### To list pending jobs

```bash
[user@server1]$ atq
```

### To remove a job (use id from atq)

```bash
[user@server1]$ atrm {id}
```
