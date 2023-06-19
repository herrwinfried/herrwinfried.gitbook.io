---
description: OpenSUSE Tumbleweed Nvidia kurulumu hakkında rehber
---

# 🚚 Nvidia Sürücüleri Yükleme

{% hint style="warning" %}
Bu rehber sırasında terminal kullanılacaktır.
{% endhint %}

{% hint style="danger" %}
Eğer ekran kartınız Geforce 400 serilerinden önce bir ekran kartına sahip iseniz maalesef opensuse tarafında bir nvidia sürücü desteği bulunmamaktadır.
{% endhint %}

## 1. Adım: Sistem Güncelleyin



Sistemin güncelliğinden emin olalım.

```bash
sudo zypper dup -y
```

Eğer güncelleştirme yaptıysa sistemi yeniden başlatınız.

## 2. Adım: Nvidia Driver Deposunu Eklemek

```bash
sudo zypper addrepo --refresh https://download.nvidia.com/opensuse/tumbleweed NVIDIA
```

```
sudo zypper --gpg-auto-import-keys refresh
```

## 3. Adım: Nvidia Sürücü Kurulumu

Şimdi Kurulumu gerçekleştirelim.

{% hint style="danger" %}
Eğer ekran kartınız Geforce 400 serilerinden önce bir ekran kartına sahip iseniz maalesef opensuse tarafında bir nvidia sürücü desteği bulunmamaktadır.
{% endhint %}

{% hint style="danger" %}
Security Boot açık ise nvidia yükledikten sonra MOK İmzalaması yapmaktadır. [Daha Fazla Bilgi](nvidia-sueruecueleri-yuekleme.md#mok-nedir)
{% endhint %}



### Geforce 700 ve Sonrası

{% hint style="warning" %}
GeForce 700 serisi ve daha yenisi için NVIDIA grafik sürücüsü kullanıyor iseniz indirmeniz gereken nvidiaG06 ile biten paketlerdir
{% endhint %}

{% code overflow="wrap" %}
```bash
sudo zypper --gpg-auto-import-keys install -y -l nvidia-glG06 x11-video-nvidiaG06 nvidia-drivers-G06
```
{% endcode %}

### Geforce 600 ve Sonrası

{% hint style="warning" %}
GeForce 600 serisi ve daha yenisi için NVIDIA grafik sürücüsü kullanıyor iseniz indirmeniz gereken nvidiaG05 ile biten paketlerdir
{% endhint %}

{% code overflow="wrap" %}
```bash
sudo zypper --gpg-auto-import-keys install -y -l nvidia-glG05 x11-video-nvidiaG05 nvidia-drivers-G05
```
{% endcode %}

### Geforce 400 ve Sonrası

{% hint style="warning" %}
GeForce 400 serisi ve daha yenisi için NVIDIA grafik sürücüsü kullanıyor iseniz indirmeniz gereken nvidiaG04 ile biten paketlerdir
{% endhint %}

{% code overflow="wrap" %}
```bash
sudo zypper --gpg-auto-import-keys install -y -l nvidia-glG04 x11-video-nvidiaG04 nvidia-drivers-G04
```
{% endcode %}

## prime-select nedir?

prime-select komutu ekran kartınız için seçim yapmanızı sağlamaktadır.

{% hint style="info" %}
intel2 yani açık kaynaklı sürücü kullanmak isterseniz yüklemeniz gereken bağımlılık mevcut

`sudo zypper --gpg-auto-import-keys install -y xf86-video-intel`
{% endhint %}

* `intel`: modeset sürücüsünü kullan
* `intel2`: Açık kaynak intel sürücüsünü kullan (xf86-video-intel)
* `nvidia`: Orjinal NVIDIA sürücüsünü kullanın
* `offload`: PRIME Render Offload Kullan (>= 435.xx sürücüsü ile mümkündür)

```bash
sudo prime-select offload
```

#### offload modu tam olarak nedir?

offload modu 435 ve üstü sürücülerde intel ve nvidia birlikte çalışabilceği bir moddur.&#x20;

örneğin sistem intel ile başlar fakat X bir uygulama açarken parametre eklerseniz intel yerine nvidia ile çalışmaya başlar.

#### Peki offload çalışıcak intel sürümünü seçebiliyor muyum?

evet isterseniz intel veya intel2 sürücüsünden biri seçebiliyorsunuz intel kısmı için. Bunun için aşağıdaki komutu kullanmanız gerekiyor.

```bash
sudo prime-select offload-set intel
```

veya

```bash
sudo prime-select offload-set intel2
```

#### Nvidia güç seçenekleri Aktifleştirme

```bash
sudo systemctl enable nvidia-hibernate.service nvidia-suspend.service nvidia-resume.service
```

#### Peki nvidia ile başlatmak istersem ne yapmam gerekiyor?

şuan için önerebilceğim yöntem maalesef ki terminal üzerine olucaktır.

```bash
__NV_PRIME_RENDER_OFFLOAD=1 __GLX_VENDOR_LIBRARY_NAME=nvidia minetest
```

buradaki minetest uygulamanın adıdır.



[Daha fazla bilgi için (İngilizce)](https://download.nvidia.com/XFree86/Linux-x86\_64/435.17/README/primerenderoffload.html)

## MOK Nedir?

Makine Sahibi Anahtarı (MOK) Güvenli Önyükleme, bir hedefin yükleyicileri, çekirdekleri ve kullanıcı tarafından sağlanan anahtarlarla imzalanmış diğer ikili dosyaları kullanarak önyükleme yapmasına izin veren alternatif bir anahtar yönetim sistemidir.

### Nvidia sürücümü kurdum ama yeniden başlattıktan sonra ne yapıcağım?

Yeniden başlattıktan sonra sırasıyla şu adımları yapmalısınız.

{% hint style="info" %}
Yön tuşlarıyla aşağı ve yukarı yapabilirsiniz.
{% endhint %}



1. <mark style="color:red;">Enroll Mok Seçin ve enter tuşuna basın</mark>
2. <mark style="color:red;">Continue Seçin ve enter tuşuna basın</mark>
3. <mark style="color:red;">Yes seçin ve enter tuşuna basın</mark>
4. <mark style="color:red;">Parola isteyecek sizden ekranda gözükmeyecektir. Parolanız Root şifresidir ve NumPad çalışmayabilir. Şifrenizi girin</mark>
5. <mark style="color:red;">Reboot seçin ve enter tuşuna basın</mark>

<figure><img src="../../../.gitbook/assets/image (95).png" alt=""><figcaption><p>Örnek Görsel OpenSUSE Wikipedia alıntılanmıştır.</p></figcaption></figure>

