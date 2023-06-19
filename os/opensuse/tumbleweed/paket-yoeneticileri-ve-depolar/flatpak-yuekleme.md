---
description: OpenSUSE Tumbleweed flatpak yükleme hakkında rehber
---

# Flatpak Yükleme

## Flatpak nedir?

Flatpak, Tıpkı zypper gibi bir paket yöneticisidir fakat paketler burada izole bir şekilde tutulur. Ve Uygulama geliştiricisinin buraya yüklediği uygulama flatpak destekleyen her işletim sisteminde çalışmaktadır.



## Nasıl Yüklenir?

{% hint style="warning" %}
Bu rehber sırasında terminal kullanılacaktır.
{% endhint %}

Aşağıdaki komutu yazalım.

```bash
sudo zypper --gpg-auto-import-keys in -y flatpak
```

{% hint style="info" %}
DNF ile yüklemek isterseniz:

```bash
sudo dnf in -y flatpak
```
{% endhint %}

{% hint style="warning" %}
Başarı ile tamamlandıktan sonra flatpak deposunu eklememiz gerekmektedir eklemek için aşağıdaki komutu yazalım.

{% code overflow="wrap" %}
```bash
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```
{% endcode %}
{% endhint %}

### KDE Store için Mağaza Desteği

KDE(discover) mağazasını kullanıyor iseniz flatpak kolayca entegre edebilceğiniz bir eklenti (Paket) mevcuttur.

<pre class="language-bash"><code class="lang-bash"><strong>sudo zypper --gpg-auto-import-keys in -y discover-backend-flatpak
</strong></code></pre>

{% hint style="info" %}
DNF ile yüklemek isterseniz:

```bash
sudo dnf in -y discover-backend-flatpak
```
{% endhint %}

Herşey başarılı ise bilgisayarınızı yeniden başlatınız.

