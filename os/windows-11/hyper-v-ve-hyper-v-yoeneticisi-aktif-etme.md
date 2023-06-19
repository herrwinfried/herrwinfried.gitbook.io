---
description: Windows 10 & 11 'de Hyper-V aktif etme
---

# 📦 Hyper-V ve Hyper-V yöneticisi aktif etme

* [Terminal Üzerinden](hyper-v-ve-hyper-v-yoeneticisi-aktif-etme.md#terminal-uezerinden)
* [Grafiksel Arayüz Üzerinden](hyper-v-ve-hyper-v-yoeneticisi-aktif-etme.md#grafiksel-arayuez-uezerinden)

### Grafiksel Arayüz Üzerinden

&#x20;Denetim Masasını açınız. Ardından <mark style="color:yellow;">"Programlar"</mark> kısmına giriniz.

<figure><img src="../../.gitbook/assets/image (218).png" alt=""><figcaption></figcaption></figure>

<mark style="color:blue;">Programlar ve Özellikler</mark> altındaki <mark style="color:yellow;">"Windows özelliklerini aç veya Kapat"</mark> Tıklayınız.

<figure><img src="../../.gitbook/assets/image (207).png" alt=""><figcaption></figcaption></figure>

1. <mark style="color:yellow;">"Hyper-V"</mark> ve içindekileri işaretleyiniz.
2. <mark style="color:yellow;">"Sanal Makine Platformu"</mark> İşaretleyiniz
3. <mark style="color:yellow;">"Windows Hiper Yöneticisi Platformu"</mark> İşaretleyiniz.
4. Tamam Basın.
5. <mark style="color:red;">**Bilgisayarınızı yeniden başlatın.**</mark>

<figure><img src="../../.gitbook/assets/image (199).png" alt=""><figcaption></figcaption></figure>

### Terminal Üzerinden

<mark style="color:red;">**Yönetici olarak**</mark> <mark style="color:blue;">Powershell veya cmd açınız.</mark>

<mark style="color:purple;">Aşağıdaki komutları teker teker yazınız.</mark>

{% code overflow="wrap" %}
```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Hyper-V-All /all /norestart
```
{% endcode %}

{% code overflow="wrap" %}
```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```
{% endcode %}

```powershell
dism.exe /online /enable-feature /featurename:HypervisorPlatform /all /norestart
```

<mark style="color:green;">**Bilgisayarınızı yeniden başlatınız.**</mark>
