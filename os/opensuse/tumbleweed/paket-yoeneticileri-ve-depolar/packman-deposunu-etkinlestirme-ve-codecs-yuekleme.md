---
description: OpenSUSE Tumbleweed packman etkinleştirme ve Codecs yükleme hakkında rehber
---

# Packman deposunu etkinleştirme ve Codecs yükleme

{% hint style="warning" %}
Bu rehber sırasında terminal kullanılacaktır.
{% endhint %}

{% hint style="danger" %}
DNF üzerinden yüklemeniz önerilmemektedir.
{% endhint %}

## Packman Deposu

Aşağıdaki komutları yazalım.

{% code overflow="wrap" %}
```bash
sudo zypper ar -cfp 90 https://ftp.gwdg.de/pub/linux/misc/packman/suse/openSUSE_Tumbleweed/ packman
```
{% endcode %}

{% code overflow="wrap" %}
```bash
sudo zypper --gpg-auto-import-keys dup -y --from packman --allow-vendor-change
```
{% endcode %}

Herşey yolunda gitti ise başarıyla packman deposunu ekledik ve normal olarak yüklediğimiz paketler packman 'da var ise packman dakiler ile değişmesini istedik.

## Codecs Yükleme

{% code overflow="wrap" %}
```bash
sudo zypper --gpg-auto-import-keys install -y --from packman ffmpeg gstreamer-plugins-{good,bad,ugly,libav} libavcodec-full vlc-codecs
```
{% endcode %}
