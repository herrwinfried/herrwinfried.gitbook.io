---
description: OpenSUSE Tumbleweed MongoDB yükleme hakkında rehber
---

# MongoDB Yükleme

{% hint style="warning" %}
Bu rehber sırasında terminal kullanılacaktır.
{% endhint %}

Aşağıdaki Komutları yazalım...

{% code overflow="wrap" %}
```bash
sudo rpm --import https://www.mongodb.org/static/pgp/server-6.0.asc
```
{% endcode %}

{% code overflow="wrap" %}
```bash
sudo zypper --gpg-auto-import-keys addrepo --gpgcheck "https://repo.mongodb.org/zypper/suse/15/mongodb-org/6.0/x86_64/" mongodb
```
{% endcode %}

```bash
sudo zypper --gpg-auto-import-keys -n install -y mongodb-org
```

