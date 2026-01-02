# 🚀 Instant Site Infrastructure Setup

This repository allows you to deploy the entire project to your computer with a single command. Forget the old "Download ZIP" method. Use this professional **IEX-style** terminal command to install everything to your Desktop with a "hacker-style" system animation.

### ⚡ One-Line Auto-Deployment (PowerShell)

Copy the code below, paste it into your **PowerShell** terminal, and watch the files deploy instantly:

```powershell
$d=[Environment]::GetFolderPath('Desktop')+'\ExampleWeb'; mkdir $d -F; write-host '--- ESTABLISHING SYSTEM CONNECTION ---' -Fore Green; iwr '[https://github.com/eymenmeral518ta-ux/eymenmeral518ta-ux.github.io/archive/refs/heads/main.zip](https://github.com/eymenmeral518ta-ux/eymenmeral518ta-ux.github.io/archive/refs/heads/main.zip)' -OutFile 'temp.zip'; Expand-Archive 'temp.zip' -Dest $d -F; gci "$d\*-main" | %{ mv $_.FullName'*' $d; rm $_.FullName -Recurse }; rm 'temp.zip'; gci $d | %{ sleep -m 150; write-host "TRANSFERRING COMPONENT >> $($_.Name)" -Fore Green }; write-host '--- DEPLOYMENT SUCCESSFUL ---' -Fore Cyan; start $d

