---
description: Hyper-v açık olmasına rağmen çalışmıyor hakkında çözüm önerim
---

# 🚁 Hyper-v açık olmasına rağmen çalışmıyor

Windows Terminalizi açın ve powershell / cmd seçin.

ve aşağıdaki komutları yazın

```
bcdedit /set hypervisorlaunchtype auto
```

```
DISM /Online /Enable-Feature /All /FeatureName:Microsoft-Hyper-V /
```
