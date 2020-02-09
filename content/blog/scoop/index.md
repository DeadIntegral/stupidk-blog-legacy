---
title: 윈도우를 위한 커맨드라인 Scoop
date: "2020-01-29"
description: "A command-line installer for Windows"
---

# required
Powershell 5 이상, .NET Framework 4.5 이상 버전 필요
```
Invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://get.scoop.sh')
# or shorter
iwr -useb get.scoop.sh | iex
# 오류 발생 시 다음과 같이 입력
Set-ExecutionPolicy RemoteSigned -scope CurrentUser
```