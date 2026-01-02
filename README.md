# 🚀 Instant Project Deployment

This repository is designed for rapid local deployment. Instead of manually downloading and moving files, you can use the professional **IEX-style** PowerShell command to install the project directly to your Desktop with a system-loading animation.

### ⚡ One-Line Setup (PowerShell)

Copy the code below, paste it into your **PowerShell** terminal, and press `Enter`:

```powershell
$d=[Environment]::GetFolderPath('Desktop')+'\ExampleWeb'; mkdir $d -F; write-host '--- INITIALIZING SECURE DOWNLOAD ---' -Fore Green; iwr '[https://github.com/eymenmeral518ta-ux/ExampleWeb/archive/refs/heads/main.zip](https://github.com/eymenmeral518ta-ux/ExampleWeb/archive/refs/heads/main.zip)' -OutFile 'temp.zip'; Expand-Archive 'temp.zip' -Dest $d -F; gci "$d\ExampleWeb-main" | %{ mv $_.FullName'*' $d; rm $_.FullName -Recurse }; rm 'temp.zip'; gci $d | %{ sleep -m 150; write-host "INJECTING COMPONENT >> $($_.Name)" -Fore Green }; write-host '--- SYSTEM DEPLOYED SUCCESSFULLY ---' -Fore Cyan; start $d
