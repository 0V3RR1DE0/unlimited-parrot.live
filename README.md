# unlimited-parrot.live
unlimited parrot.live


```
powershell -WindowStyle Hidden -Command "$timer = [System.Diagnostics.Stopwatch]::StartNew(); while($true) { if (!(Get-Process -Name cmd -ErrorAction SilentlyContinue | Where-Object {$_.MainWindowTitle -eq 'parrot.live'})) { Start-Process cmd.exe -ArgumentList '/c curl parrot.live' -WindowStyle Minimized }; Start-Sleep -Milliseconds 100; if($timer.Elapsed.TotalSeconds -ge 60) { $timer.Restart() } }"
```
