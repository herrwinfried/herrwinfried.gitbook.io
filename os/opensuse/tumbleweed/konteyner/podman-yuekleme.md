# Podman Yükleme

{% hint style="warning" %}
Bu rehber sırasında terminal kullanılacaktır.
{% endhint %}

Aşağıdaki komut yazalım.&#x20;

```bash
sudo zypper --gpg-auto-import-keys in -y podman
```

{% hint style="info" %}
DNF ile yüklemek isterseniz

```bash
sudo dnf install -y podman
```
{% endhint %}

ve yüklendikten sonra&#x20;

```
sudo systemctl enable --now podman.service podman.socket
```

```
systemctl --user enable --now podman.service podman.socket
```

komutlarını giriniz. Ve artık hazır!

## BONUS: Podman Desktop

{% hint style="info" %}
Flathub üzerinden indirmeniz gerekiyor. [Flathub yüklü değil ise rehberime göz atınız.](../paket-yoeneticileri-ve-depolar/flatpak-yuekleme.md#nasil-yueklenir)
{% endhint %}

```bash
flatpak install -y --user flathub io.podman_desktop.PodmanDesktop
```

<mark style="color:purple;">Eğer hata alırsanız -y çıkarın ve öyle deneyin indirmek isteyip istemediğinizi soracaktır. evet için belirtilen harf basar iseniz indirmeye başlıyacaktır.</mark>

