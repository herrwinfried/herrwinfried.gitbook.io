---
description: OpenSUSE Tumbleweed Chrome Browser Yükleme
---

# Chrome

{% hint style="warning" %}
Bu rehber sırasında terminal kullanılacaktır.
{% endhint %}

Aşağıdaki komutları sırasıyla yazalım.&#x20;

{% hint style="info" %}
Birden Fazla Yöntem ile yükliyebiliriz.
{% endhint %}

1. [Opi ile yükleme](chrome.md#1.-opi-ile-yuekleme)
2. [Web sitesine giderek yükleme](chrome.md#2.-web-sitesine-giderek-yuekleme)

## 1. Opi ile yükleme

{% hint style="info" %}
opi paketinin kurulu olması gerektiğini unutmayın eğer kurmadıysanız [buraya tıklarak nasıl kurulucağına bakınız](../paket-yoeneticileri-ve-depolar/opi-yuekleme.md#nasil-yueklenir).
{% endhint %}

```bash
opi chrome
```

Çıkan sonuçlarda brave browser deposunu ekliyim mi diye sorarsa evet işaretleyiniz<mark style="color:blue;">(Örn: Do you want to install Chrome from Google repository? (Y/n) y)</mark>

## 2. Web sitesine giderek yükleme

[https://www.google.com/chrome/](https://www.google.com/chrome/) sayfasına gidiyoruz. İndirme butonuna basıyoruz

RPM seçiyoruz ve indiriyoruz.

<figure><img src="../../../../.gitbook/assets/image (149).png" alt=""><figcaption></figcaption></figure>

İndirdiğimiz dizine gidiyoruz ve terminal açıyoruz ardından şu komutu yazıyoruz.

```bash
sudo zypper --no-gpg-checks install -y -l ./google-chrome-stable_current_x86_64.rpm
```



