# unlimited-parrot.live
unlimited parrot.live


```
powershell -WindowStyle Hidden -Command "$ErrorActionPreference = 'Stop'; while($true) { try { $existingWindows = Get-Process -Name cmd -ErrorAction SilentlyContinue | Where-Object { $_.MainWindowTitle -like '*parrot.live*' }; if ($existingWindows.Count -eq 0) { Start-Process cmd.exe -ArgumentList '/c title parrot.live && curl parrot.live' -WindowStyle Minimized; Start-Sleep -Seconds 5; } else { Start-Sleep -Seconds 60; } } catch { Start-Sleep -Seconds 5; } }"
```
