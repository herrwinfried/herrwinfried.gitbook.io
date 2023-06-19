---
description: >-
  WSL (MS Store) systemd nasıl etkinleştirebiliriz hakkında bahsettiğim
  rehberim.
---

# ⚙ WSL Systemd Etkinleştirme

{% hint style="warning" %}
Hala geliştirilmekte olup normal Linux'daki kadar düzgün çalışabilceğinin bir garantisi bulunmamaktadır.
{% endhint %}

## Dağıtım İçinden Yapılacak İşlemler

systemd aktif etmek istediğiniz dağıtımı açınız ve

`/etc/wsl.conf` dosyasın içine aşağıdakileri ekliyelim

{% code title="/etc/wsl.conf" %}
```bash
[boot]
systemd=true
```
{% endcode %}

Daha sonra WSL kapatmanız gerekmektedir. Windows Powershell veya CMD açıp aşağıdaki komutu yazınız.&#x20;

```
wsl.exe --shutdown
```

Tebrikler, Artık Systemd seçtiğiniz dağıtımda aktif olacaktır.
