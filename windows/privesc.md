# Place Holder

## 1 Get Permissions On Service Executables
- 1a. Generate list of executables
```for /f "tokens=2 delims='='" %a in ('wmic service list full^|find /i "pathname"^|find /i /v "system32"') do @echo %a >> C:\windows\temp\msntemp.tmp```
- 1b. List Permissions - \Users:(I)(F) would be nice :)
```for /f eol^=^"^ delims^=^" %a in (c:\windows\temp\msntemp.tmp) do cmd.exe /c icacls "%a"```
#### Credit
https://www.linkedin.com/pub/ben-clark/8/116/644


More content coming. Feel free to submit ;-)
