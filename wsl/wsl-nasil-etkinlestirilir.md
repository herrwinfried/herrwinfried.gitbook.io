---
description: Windows 11'de WSL (MS Store) Nasıl Etkinleştirilir Hakkında Rehber
---

# 🙇♀ WSL Nasıl Etkinleştirilir?

## Microsoft Store Üzerinden WSL

### Başlamadan Önce

#### Sanal Makine Platform Aktif Ediniz

{% hint style="danger" %}
Sanal Makine Platform ben powershell üzerinden aktif edeceğim siz isterseniz "windows özellikleri aç veya kapat" üzerindende aktif edebilirsiniz.
{% endhint %}

Windows Terminalinizi Yönetici Olarak Açınız

{% hint style="info" %}
Arama Çubuğuna Windows Terminal yazıp üstüne gelip sağ tık yapıp yönetici olarak başlat yapabilir&#x20;

veya

Windows + X basıp(veya windows logosuna sağ tık ile) Windows Terminal (yönetici) seçebilirsiniz
{% endhint %}

aşağıdaki komutu yazınız

```
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

{% hint style="warning" %}
Windows Özelliklerindeki WSL devre dışı bırakmak isterseniz şu komutu yazınız.

```
dism.exe /online /disable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```
{% endhint %}

Bilgisayarınızı yeniden başlatınız.

### İndirme & Yükleme

[https://www.microsoft.com/store/productId/9P9TQF7MRM4R](https://www.microsoft.com/store/productId/9P9TQF7MRM4R) adresine gidiyoruz Türkçe olarak açıldıysa "Al" ingilizce olarak açıldıysa "get" button basıyoruz. Ardından Microsoft store açmak istediğini belirtiyor tarayıcımız tamam basıyoruz.

![](<../.gitbook/assets/image (4).png>)

ve buradan "Yükle" veya "Al" basarak indiriyoruz. İndirme işlemleri tamamlandıktan sonra işimizin garanti olması adına

windows terminalimizi yönetici olarak açıyoruz ve aşağıdaki komutları yazıyoruz

```
wsl --set-default-version
```

ve&#x20;

```
wsl --update
```

yazıyoruz ve herşey yolunda gittiyse kurmayı başardık demektir. Bundan sonra geriye bir Distro yüklemek kalıyor.

#### WSL Etkinleştirme

#### **WSL Kurduktan sonra yapılması gerekenler \[önemli]**

Windows Terminalizi Yönetici Olarak Açınız.

{% hint style="info" %}
Arama Çubuğuna Windows Terminal yazıp üstüne gelip sağ tık yapıp yönetici olarak başlat yapabilir&#x20;

veya

Windows + X basıp(veya windows logosuna sağ tık ile) Windows Terminal (yönetici) seçebilirsiniz
{% endhint %}

aşağıdaki komutları yazınız

```
wsl --set-default-version 2
```

```
wsl --update
```

ve herşey yolunda gittiyse kurmayı başardık demektir. Bundan sonra geriye bir Distro yüklemek kalıyor.
