---
description: OpenSUSE Tumbleweed snap yükleme hakkında rehber
---

# Snap Yükleme

## Snap Store nedir?

Snap, [Flatpak ](flatpak-yuekleme.md#flatpak-nedir)ile benzer amacı taşımaktadır. Teknik Özellikler bakımından farklıdırlar.&#x20;

## Nasıl yüklenir?

İlk önce snap store deposunu yüklememiz gerekmektedir. Çünkü opensuse dahili olarak bulunmaz.

### Depoyu ekleme

{% code overflow="wrap" %}
```bash
sudo zypper --gpg-auto-import-keys addrepo --refresh https://download.opensuse.org/repositories/system:/snappy/openSUSE_Tumbleweed snappy && sudo zypper --gpg-auto-import-keys refresh
```
{% endcode %}

{% hint style="info" %}
DNF üzerinden eklemek isterseniz.

{% code overflow="wrap" %}
```bash
sudo dnf config-manager --add-repo https://download.opensuse.org/repositories/system:/snappy/openSUSE_Tumbleweed/system:snappy.repo && sudo dnf refresh
```
{% endcode %}
{% endhint %}

### Paket yükleme

<pre class="language-bash"><code class="lang-bash"><strong>sudo zypper --gpg-auto-import-keys in -y snapd
</strong></code></pre>

{% hint style="info" %}
DNF üzerinden yüklemek isterseniz.

```bash
sudo dnf install -y snapd
```
{% endhint %}

paketi yükledikten sonra aşağıdaki komutları yazalım.

```bash
sudo systemctl enable --now snapd && sudo systemctl enable --now snapd.apparmor
```

Herşey başarılı ise bilgisayarınızı yeniden başlatınız.



