# alias

[Back](README.md) to Linux CheatSheets by Ireaneus

- Show a list of your current shell aliases:

`[user@server1] alias`

- Map 'll' to 'ls -l' Can be used per session or put inside a shell config file like .bash_aliases:

```sh
[user@server1] alias ll='ls -l'
[user@server1] alias ch='docker pull ireaneus/cheatsheet && docker run -rm -ti ireaneus/cheatsheet:latest'
```
