---
description: >-
  Microsoft Office kurulum yüklemesini nasıl özelleştirebilceğimiz hakkında
  rehber.
---

# ☕ Microsoft 365(Office) Özel Config ile yükleme

## 1. Konfigurasyon dosyası hazırlama

[https://config.office.com/deploymentsettings](https://config.office.com/deploymentsettings) adresine gidelim.

### Arch seçimi

1. 32 bit mi 64 mü indirceğinizi seçiniz. (Her ikisi için oluşturcaksanız aynısından bir tane daha oluşturmalısınız.)

<figure><img src="../.gitbook/assets/image (120).png" alt=""><figcaption></figcaption></figure>

### Products

2. Office sürümümüzü seçelim ben LTSC Pro Plus 2021 seçiceğim.
3. Visio yüklenip yüklenmiceğini seçiniz. (ben none olarak bıraktım)
4. Project yüklenip yüklenmiceğini seçiniz. (ben none olarak bıraktım)
5. Ek ürün yüklenip yüklenmiceğini seçiniz. (Ben Language pack olarak işaretledim)

<figure><img src="../.gitbook/assets/image (154).png" alt=""><figcaption></figcaption></figure>

### Update Channel

6. Güncelleme kanallarını seçiniz.&#x20;

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

### Apps

7. Hangi uygulamaların yüklenip yüklenmiceğini seçiniz.
8. Next butonuna basınız.

<figure><img src="../.gitbook/assets/image (114).png" alt=""><figcaption></figcaption></figure>

### Language

9. Birincil dil seçiniz.&#x20;
10. İkinci dil ekleyin (İsteğe bağlı)
11. İkinci dil Yazım denetleyicisi ekleyin (İsteğe bağlı)

<figure><img src="../.gitbook/assets/image (189).png" alt=""><figcaption></figcaption></figure>

### Installation

Kurulum seçeneklerinizi ayarlayınız.

<figure><img src="../.gitbook/assets/image (168).png" alt=""><figcaption></figcaption></figure>

### Upgrade Options

yükseltme seçeneklerinizi ayarlayınız.

<figure><img src="../.gitbook/assets/image (111).png" alt=""><figcaption></figcaption></figure>

### Licence



Lisans ayarlarını yapınız.

<figure><img src="../.gitbook/assets/image (163).png" alt=""><figcaption></figcaption></figure>

### Application preferences



Uygulamalar için ayarları yapınız.

<figure><img src="../.gitbook/assets/image (182).png" alt=""><figcaption></figcaption></figure>

Finish buttonuna basınız.

### Finish

"Export" Seçeneğine tıklıyalım.

<figure><img src="../.gitbook/assets/image (172).png" alt=""><figcaption></figcaption></figure>

"Office Open XML Formats" olarak işaretleyin ve ilerleyin.

<figure><img src="../.gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>

#### Sözleşmeyi kabul ediniz ve Export buton tıklayınız.

<figure><img src="../.gitbook/assets/image (136).png" alt=""><figcaption></figcaption></figure>

## 2. Office Deployment tool indirme

[https://www.microsoft.com/en-us/download/details.aspx?id=49117](https://www.microsoft.com/en-us/download/details.aspx?id=49117) adresine gidelim.

"Download" tıklayın.

<figure><img src="../.gitbook/assets/image (151).png" alt=""><figcaption></figcaption></figure>

## 3. odt (Office deployment tool) çalıştırma

2. [Adımda indirdiğimiz dosyanın ismini](microsoft-365-office-oezel-config-ile-yuekleme.md#2.-office-deployment-tool-indirme) odt olarak değiştirelim&#x20;

A. cmd veya powershell açalım.

B. İndirdiğiniz dosyanın bulunduğu konuma gidelim.

{% code overflow="wrap" %}
```powershell
.\odt.exe /extract:C:/office365
```
{% endcode %}

config dosyamızı extract çıkardığımız klasöre yerleştirelim.

C diskinde office365 adında ki klasöre gidip `Configuration.xml` adlı dosyanızı yapıştırınız.

Ardından&#x20;

```powershell
cd C:/office365
```

#### Offline kurulum için önceden indirelim.

```powershell
.\setup.exe /download .\Configuration.xml
```

#### Kurulum Geçelim&#x20;

{% hint style="info" %}
Online kurulum için download yerine direkt bunu yazabilirsiniz.
{% endhint %}

```powershell
.\setup.exe /configure .\Configuration.xml
```

ve işlem tamamlandı!!
