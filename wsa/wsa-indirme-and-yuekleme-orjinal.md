---
description: Orjinal WSA Nasıl indirebilceğimiz hakkında rehberim.
---

# 🙌 WSA İndirme & Yükleme \[Orjinal]

## Başlamadan Önce

* [Sanal Makine Platform](wsa-indirme-and-yuekleme-orjinal.md#sanal-makine-platform-etkinlestirme)

### Sanal Makine Platform Etkinleştirme

{% hint style="info" %}
Windows Özellikleri aç veya kapat üzerindende etkinleştirebilir.
{% endhint %}

Windows Terminalizi Yönetici Olarak Çalıştırın.

```
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

{% hint style="warning" %}
Sanal Makine Platform aktifleştirdikten sonra bilgisarınızı yeniden başlatmak gerekebilir.
{% endhint %}

İki Method Mevcuttur

* [Microsoft Store üzerinden indirme](wsa-indirme-and-yuekleme-orjinal.md#ms-store-uezerinden-yuekleme)
* [https://store.rg-adguard.net/ sayfası üzerinden indirme](wsa-indirme-and-yuekleme-orjinal.md#ms-store-disindan-yuekleme)

## MS Store Üzerinden Yükleme

[https://www.microsoft.com/store/productId/9P3395VX91NR](https://www.microsoft.com/store/productId/9P3395VX91NR) adresine gidiyoruz Türkçe olarak açıldıysa "Al" ingilizce olarak açıldıysa "get" button basıyoruz. Ardından Microsoft store açmak istediğini belirtiyor tarayıcımız tamam basıyoruz.

![](<../.gitbook/assets/image (59).png>)

ve buradan "Yükle" veya "Al" basarak indiriyoruz.

ve işlem başarılı.

## MS Store dışından Yükleme

### İndirme

ilk önce [https://store.rg-adguard.net/](https://store.rg-adguard.net/) bağlantılı sayfaya gidiyoruz ve birkaç adımı yapıyoruz.

1. İlk Button "URL (Link)" Olarak seçiniz.
2. URL olarak yazılması gereken yere "[https://www.microsoft.com/store/productId/9P3395VX91NR](https://www.microsoft.com/store/productId/9P3395VX91NR)" yazınız.
3. Varsayınal "RP" Seçili olan button "Slow" olarak seçiniz.
4. Tik işaretine basın ve aratın.

Aşağıdaki görsel gibi olması gerekiyor.

![](<../.gitbook/assets/image (89).png>)

"MicrosoftCorporationII.WindowsSubsystemForAndroid\_1.7.32815.0\_neutral\_\~\_8wekyb3d8bbwe.msixbundle" adlı dosyayı bulunuz

{% hint style="info" %}
NOT: Siz bu rehbere baktığınızda yeni bir sürüm çıkabilir o yüzden 1,2 GB+ olmasına dikkat ederek daha rahat bulabilirsiniz sonu ".msixbundle" ile bitmesinede dikkat edin
{% endhint %}

![](<../.gitbook/assets/image (92).png>)

### Yükleme

{% hint style="info" %}
Aşağıdaki işlemleri denemeden önce dosyaya gidip çift tıklama yapın eğer oradan yükleniyorsa aşağıdaki komutları yazmanız gerekmez.
{% endhint %}

Windows Terminali yönetici olarak başlatın. Windows Powershell seçin.

Powershell 7 seçerseniz ilk önce

```
Import-Module -Name Appx -Use WindowsPowershell
```

msixbundle dosyasını indirdiğiniz konuma gidin.\
Ben masaüstüne indirdiğinizi varsayarak ilerlicem.

```
cd .\Desktop\
```

{% hint style="info" %}
Tab tuşuna basarsanız size kelime tamamlamada yardım edecektir.
{% endhint %}

ve işlem bu kadar!
