---
description: OpenSUSE Tumbleweed opi yükleme hakkında rehber
---

# Opi Yükleme

## Opi Nedir?

Opi, Open Build Service, Üçüncü Parti depolardan, Packman deposundan sizlere istediğiniz paketi yüklemenizi sağlıyan basit bir CLI(Komut Satırı Arayüz) 'dir.

## Nasıl Yüklenir?

{% hint style="warning" %}
Bu rehber sırasında terminal kullanılacaktır.
{% endhint %}

Aşağıdaki komutu yazalım.

```bash
sudo zypper --gpg-auto-import-keys in -y opi
```

{% hint style="info" %}
DNF ile yüklemek isterseniz:

```bash
sudo dnf in -y opi
```
{% endhint %}

Yukarıdaki komutu yazdıktan sonra mevcut terminalinizi kapatınız ve tekrar açınız ardından `opi UygulamaAdı` yazdıktan sonra sizlere seçenek sunup istediğiniz uygulamayı bilgisayarınıza yükleyip yüklemek istemediğinizi soracaktır.

