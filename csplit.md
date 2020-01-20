# csplit

[Back](README.md) to Linux CheatSheets by Ireaneus

Split a file based on pattern

```bash
csplit input.file '/PATTERN/'
```

Use prefix/suffix to improve resulting file names

```bash
csplit -f 'prefix-' -b '%d.extension' input.file '/PATTERN/' '{*}'

```
