---
description: OpenSUSE Tumbleweed Microsoft Edge Yükleme
---

# Microsoft Edge

{% hint style="warning" %}
Bu rehber sırasında terminal kullanılacaktır.
{% endhint %}

Aşağıdaki komutları sırasıyla yazalım.&#x20;

{% hint style="info" %}
Birden Fazla Yöntem ile yükliyebiliriz.
{% endhint %}

1. [Opi ile yükleme](microsoft-edge.md#1.-opi-ile-yuekleme)
2. [Zypper ile yükleme](microsoft-edge.md#2.-zypper-ile-yuekleme)
3. [Dnf ile yükleme](microsoft-edge.md#3.-dnf-ile-yuekleme)

## 1. Opi ile yükleme

{% hint style="info" %}
opi paketinin kurulu olması gerektiğini unutmayın eğer kurmadıysanız [buraya tıklarak nasıl kurulucağına bakınız](../paket-yoeneticileri-ve-depolar/opi-yuekleme.md#nasil-yueklenir).
{% endhint %}

```bash
opi msedge
```

Çıkan sonuçlarda brave browser deposunu ekliyim mi diye sorarsa evet işaretleyiniz<mark style="color:blue;">(Örn: Do you want to install Microsoft Edge from Microsoft repository? (Y/n) y)</mark>



## 2. Zypper ile yükleme

```bash
sudo zypper --gpg-auto-import-keys in -y curl
```

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
```

```bash
sudo zypper addrepo https://packages.microsoft.com/yumrepos/edge/config.repo
```

<pre class="language-bash"><code class="lang-bash"><strong>sudo zypper --gpg-auto-import-keys in -y Microsoft-edge-stable
</strong></code></pre>

## 3. Dnf ile yükleme

{% hint style="info" %}
dnf kurulu olması gerekmektedir.[ Kurmak için burayı inceleyiniz.](../paket-yoeneticileri-ve-depolar/dnf-yuekleme.md#nasil-yueklenir)
{% endhint %}

```bash
sudo dnf install -y curl
```

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
```

{% code overflow="wrap" %}
```bash
sudo dnf config-manager --add-repo https://packages.microsoft.com/yumrepos/edge/config.repo
```
{% endcode %}

<pre class="language-bash"><code class="lang-bash"><strong>sudo dnf install -y microsoft-edge-stable
</strong></code></pre>
