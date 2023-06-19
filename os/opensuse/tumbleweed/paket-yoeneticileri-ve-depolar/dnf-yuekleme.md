---
description: OpenSUSE Tumbleweed dnf yükleme hakkında rehber
---

# DNF Yükleme

## DNF nedir?

DNF, Tıpki Zypper gibi bir paket yöneticisidir.

## Nasıl Yüklenir?

Aşağıdaki komutları yazalım.

{% code overflow="wrap" %}
```bash
sudo zypper --gpg-auto-import-keys in -y dnf rpm-repos-openSUSE-Tumbleweed
```
{% endcode %}

```bash
sudo dnf makecache
```

#### PackageKit'de dnf kullanmak istiyorum!

```bash
sudo zypper --gpg-auto-import-keys in -y PackageKit-backend-dnf
```

```bash
sudo dnf swap PackageKit-backend-zypp PackageKit-backend-dnf
```

### DNF Plugin yüklemek isterseniz

{% code overflow="wrap" %}
```bash
sudo zypper --gpg-auto-import-keys in -y dnf-plugins-core
```
{% endcode %}
