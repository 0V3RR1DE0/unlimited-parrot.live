# unlimited-parrot.live
unlimited parrot.live


```
powershell -windowstyle hidden -command "& {while ($true) {if (-not (Get-Process | Where-Object {$_.MainWindowTitle -eq 'parrot'})) {Start-Process cmd -ArgumentList '/c title parrot & curl parrot.live & pause'}}}"
```
