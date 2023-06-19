---
description: >-
  WSA'ya Nasıl Google Play store ve google servisleri yüklenebilceği hakkında
  rehberim
---

# 🖥 WSA Dahili Olarak Google Servisleri Yükleme

{% hint style="danger" %}
Her ne kadar yapıcağımız işlem basit olsada deneyseldir. Kendi bilincinizde yapınız sorumluluk almıyorum.
{% endhint %}

{% hint style="danger" %}
Bu yöntem ile güncelleme alamıcaksınız WSA'dan. Bir güncelleme geldimi herşeyi silip tekrar yüklemeniz gerekicek.
{% endhint %}

{% hint style="success" %}
Bu Rehberde Kendi yaptığım grafiksel arayüzlü taşınabilir bir programı kullanıcaz. Bizim yazmamız gereken dosyaları otomatik olarak powershell çalıştırıp yapıcaktır.
{% endhint %}

## Gerekliler

<mark style="color:yellow;">**Biz bu rehberimizde bunları otomatik halleden script deniyeceğiz.**</mark>

## Ön Hazırlık

[https://github.com/herrwinfried/EasierWsaInstallerGui/releases](https://github.com/herrwinfried/EasierWsaInstallerGui/releases) Sayfasına gidiyoruz.

<figure><img src="../.gitbook/assets/image (161).png" alt=""><figcaption></figcaption></figure>

En güncel sürümünü seçip zip dosyasını indiriyoruz.

<figure><img src="../.gitbook/assets/image (109).png" alt=""><figcaption></figcaption></figure>

Ardından indirdiğimiz zip üstüne gelip "Tümünü Ayıkla..." basın.

<figure><img src="../.gitbook/assets/image (195).png" alt=""><figcaption></figcaption></figure>

Ardından Ayıkla basınız.&#x20;

<figure><img src="../.gitbook/assets/image (180).png" alt=""><figcaption></figcaption></figure>

Ardından ayıklanan klasörün içine giriniz ve EasierWsaInstaller.Desktop(.exe) Uygulamasını bulup ve çift tıklayın.

<figure><img src="../.gitbook/assets/image (160).png" alt=""><figcaption></figcaption></figure>

Böyle bir ekran ile karşılaşırsanız "Ek Bilgi..." Ardından "Yine de çalıştır" butonuna basınız.

<figure><img src="../.gitbook/assets/image (135).png" alt=""><figcaption></figcaption></figure>

Açılcak olan ekranda "önkoşulları yükle" butonuna basınız.

{% hint style="danger" %}
Açılıcak olan pencerede 1-2 kere yönetici izni istiyecektir Yönetici iznini vermelisiniz aksi taktirde işlem başarısız olacaktır.
{% endhint %}

<mark style="color:red;">**İşlem tamamlandıktan sonra bilgisayarınızı yeniden başlatınız.**</mark>

### Önhazırlık - Yeniden Başlattıktan sonra

<figure><img src="../.gitbook/assets/image (126).png" alt=""><figcaption></figcaption></figure>

Başlat menünüze gelip Ubuntu adlı uygulamayı bulunuz ve üstüne çift tıklayınız.

<figure><img src="../.gitbook/assets/image (158).png" alt=""><figcaption></figcaption></figure>

&#x20;Bir kullanıcı adı ve şifre giriniz sırasıyla. <mark style="color:red;">Şifre Oluştururken yazdığınız karakterler güvenlik gerekçesi ile gözükmicektir.</mark>

<figure><img src="../.gitbook/assets/image (165).png" alt=""><figcaption></figcaption></figure>

Böyle olduğu durumda ekranı kapatabiliriz. Ardından Kuruluma geçelim!

## Kurulum

EasierWsaInstaller uygulamasın klasörünü açalım.

<figure><img src="../.gitbook/assets/image (180).png" alt=""><figcaption></figcaption></figure>

EasierWsaInstaller.Desktop(.exe) Uygulamasını bulup ve çift tıklayın.

<figure><img src="../.gitbook/assets/image (160).png" alt=""><figcaption></figcaption></figure>

Böyle bir ekran ile karşılaşırsanız "Ek Bilgi..." Ardından "Yine de çalıştır" butonuna basınız.

<figure><img src="../.gitbook/assets/image (196).png" alt=""><figcaption></figcaption></figure>

_<mark style="color:green;">Yeşil ile işaretlenmiş alan dışındakilerin değerini değiştirmemeniz önerilir.</mark>_

Hazır Button basınız ve Açılıcak olan yönetici iznine izin veriniz. Ardından arkanıza yaslanın.



Eğer İsteğe bağlı seçeneklerinden "İndirdikten sonra kur" işaretli ise bilgisayarınıza kendisi kurulumu gerçekleştircektir.

