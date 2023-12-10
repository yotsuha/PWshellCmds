# PWshell Cheatsheet

<details><summary><h3>PWshell equivalents of Linux commands</h3></summary>

#### PWshell equivalent of 'man [command]'
```
# Aliases: None
Get-Help [command]
```

#### PWshell equivalent of 'ls -laR'
```
# Aliases: gci, ls, dir
Get-ChildItem -Force -Recurse
```

#### PWshell equivalent of 'rm -rf [file]'
```
# Aliases: ri, rm, rmdir, del, erase, rd
Remove-Item -Recurse -Force [file]
```

#### PWshell command history file location.
```
# to check path to history file
(Get-PSReadlineOption).HistorySavePath
```

#### PWshell equivalent of 'systemctl status [service] || service [service] status'
```
# Alias: gsv
Get-Service [service] || Service [service]
```

#### PWshell equivalent of 'systemctl start [service] || service [service] start'
```
# Alias: sasv
Start-Service [service]
```

#### PWshell equivalent of 'systemctl stop [service] || service [service] stop'
```
# Alias: spsv
Stop-Service [service]
```
</details>
