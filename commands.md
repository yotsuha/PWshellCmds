# PWshell Cheatsheet

<details><summary><h3>PWshell equivalents of Linux commands</h3></summary>

#### PWshell equivalent of 'bash -c "[command] &"' (running script in the backgroud/hidden)
```
# Aliases: None
PowerShell -WindowStyle Hidden -Command [command]
```

#### PWshell command to get items from an object
```
Aliases: None
([object]).[item]
```

#### PWshell equivalent of 'man [command]'
```
# Aliases: None
Get-Help [command]
```

#### PWshell equivalent of 'cat [file] | grep [string]'
```
# Alias: sls
Get-Content [file] | Select-String [string]
```

#### PWshell equivalent of 'echo [string]'
```
# Aliases: write, echo
Write-Output [string]
```

#### PWshell equivalent of 'echo [string] >&2'
```
# Aliases: write, echo
Write-Error [string]
```

#### PWshell equivalent of 'ls -laR'
```
# Aliases: gci, ls, dir
Get-ChildItem -Force -Recurse
```

#### PWshell equivalent of 'cp [target] [destination]'
```
# Aliases: cpi, cp, copy
Copy-Item [target] [destination]
```

#### PWshell equivalent of 'cp [target] [destination]'
```
# Aliases: mi, mv, move
Move-Item [target] [destination]
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

#### PWshell equivalent of "cat /etc/passwd | awk -F: '{print $1}'"
```
# Alias: glu
Get-LocalUser
```

#### PWshell equivalent of 'useradd [user]'
```
Alias: nlu
New-LocalUser [user]
```

#### PWshell equivalent of 'userdel [user]'
```
Alias: rlu
Remove-LocalUser [user]
```

#### PWshell equivalent of 'usermod -l [newname] [oldname]
```
Alias: rnlu
Rename-LocalUser [oldname] [newname]
```

#### PWshell equivalent of 'usermod [user] [args]'
```
Alias: slu
Set-LocalUser [user] [args]
```

#### PWshell equivalent of 'usermod -L -e 1 [user] || usermod -e 1 [user] && passwd -l [user]'
```
Alias: dlu
Disable-LocalUser [user]
```

#### PWshell equivalent of 'usermod -U -e "" [user] || usermod -e "" [user] && passwd -u [user]'
```
Alias: elu
Enable-LocalUser [user]
```

#### PWshell equivalent of "cat /etc/group | awk -F: '{print $1}'"
```
Alias: glg
Get-LocalGroup
```

#### PWshell equivalent of 'groupadd [group]'
```
Alias: nlg
New-LocalGroup [group]
```

#### PWshell equivalent of 'groupdel [group]'
```
Alias: rlg
Remove-LocalGroup [group]
```

#### PWshell equivalent of 'groupmod -n [newgroupname] [oldgroupname]'
```
Alias: rnlg
Rename-LocalGroup [oldgroupname] [newgroupname]
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
