---
description: OpenSUSE Tumbleweed Brave Browser Yükleme
---

# Brave Browser

{% hint style="warning" %}
Bu rehber sırasında terminal kullanılacaktır.
{% endhint %}

Aşağıdaki komutları sırasıyla yazalım.&#x20;

{% hint style="info" %}
Birden Fazla Yöntem ile yükliyebiliriz.
{% endhint %}

1. [Opi ile yükleme](brave-browser.md#1.-opi-ile-yuekleme)
2. [Zypper ile yükleme](brave-browser.md#2.-zypper-ile-yuekleme)
3. [Dnf ile yükleme](brave-browser.md#3.-dnf-ile-yuekleme)

## 1. Opi ile yükleme

{% hint style="info" %}
opi paketinin kurulu olması gerektiğini unutmayın eğer kurmadıysanız [buraya tıklarak nasıl kurulucağına bakınız](../paket-yoeneticileri-ve-depolar/opi-yuekleme.md#nasil-yueklenir).
{% endhint %}

```bash
opi brave-browser
```

Çıkan sonuçlarda brave browser deposunu ekliyim mi diye sorarsa evet işaretleyiniz<mark style="color:blue;">(Örn: Do you want to install Brave from Brave repository? (Y/n) y)</mark>



## 2. Zypper ile yükleme

```bash
sudo zypper --gpg-auto-import-keys in -y curl
```

```bash
sudo rpm --import https://brave-browser-rpm-release.s3.brave.com/brave-core.asc
```

```bash
sudo zypper addrepo https://brave-browser-rpm-release.s3.brave.com/brave-browser.repo
```

<pre class="language-bash"><code class="lang-bash"><strong>sudo zypper --gpg-auto-import-keys in -y brave-browser
</strong></code></pre>

## 3. Dnf ile yükleme

{% hint style="info" %}
dnf kurulu olması gerekmektedir.[ Kurmak için burayı inceleyiniz.](../paket-yoeneticileri-ve-depolar/dnf-yuekleme.md#nasil-yueklenir)
{% endhint %}

```bash
sudo dnf install -y curl
```

```bash
sudo rpm --import https://brave-browser-rpm-release.s3.brave.com/brave-core.asc
```

{% code overflow="wrap" %}
```bash
sudo dnf config-manager --add-repo https://brave-browser-rpm-release.s3.brave.com/brave-browser.repo
```
{% endcode %}

<pre class="language-bash"><code class="lang-bash"><strong>sudo dnf install -y brave-browser
</strong></code></pre>
