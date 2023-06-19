# Docker Yükleme

{% hint style="warning" %}
Bu rehber sırasında terminal kullanılacaktır.
{% endhint %}

Aşağıdaki komutları yazalım.&#x20;

{% code overflow="wrap" %}
```bash
sudo zypper --gpg-auto-import-keys in -y docker docker-compose docker-compose-switch
```
{% endcode %}

{% hint style="info" %}
DNF ile yüklemek isterseniz

```bash
sudo dnf install -y docker docker-compose docker-compose-switch
```
{% endhint %}

Aşağıdaki komut arka planda çalışmasına izin vermek için gereklidir.

```bash
sudo usermod -G docker -a $USER
```

Sistem açıldığında başlatmak ister isek bu komutuda yazmamız gerekiyor.

```
sudo systemctl enable docker
```

{% hint style="warning" %}
Docker rootless olarak yüklenmediğinden sudo docker ile çalıştırmanız gerekiyor.
{% endhint %}

