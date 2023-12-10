# PWshell command history file location.
```
# to check path to history file
(Get-PSReadlineOption).HistorySavePath
```

# PWshell equivalent of 'rm -rf [file]'
```
# Aliases: ri, rm, rmdir, del, erase, rd
rm -Recurse -Force [file]
```

# PWshell equivalent of 'ls -lAR'
```
# Aliases: gci, ls, dir
ls -Force -Recurse
```

# PWshell equivalent of 'systemctl start [service] || service [service] start'
```
# Aliases: sasv
Start-Service [service]
```

# PWshell equivalent of 'systemctl stop [service] || service [service] stop'
```
# Aliases: spsv
Stop-Service [service]
```

# PWshell equivalent of 'systemctl status [service] || service [service] status'
```
# Alias: gsv
Get-Service [service]
# or
Service [service]
```
