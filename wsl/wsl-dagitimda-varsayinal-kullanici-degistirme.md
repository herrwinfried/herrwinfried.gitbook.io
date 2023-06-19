---
description: >-
  WSL (MS Store) Varsayınal Kullanıcı Nasıl Değiştirebilirsiniz hakkında
  bahsettiğim rehberim.
---

# 👨👩👦👦 WSL Dağıtım'da Varsayınal Kullanıcı Değiştirme

## Dağıtımınıza Açınız

{% hint style="info" %}
Ben bu rehberi anlatırken bash ve nano üzerinden anlatıcağım siz isterseniz başka shell ve metin editorü kullanabilirsiniz.
{% endhint %}

Dağıtımınızın Shell açınız ve&#x20;

```
nano /etc/wsl.conf
```

yazınız. Ardından metin editörümüz açıldıktan sonra aşağıdakileri yazınız

{% hint style="danger" %}
USERNAME yazan kısma kendi kullanıcı adınızı yazıcaksınız.
{% endhint %}

```
[user]
default=USERNAME
```

kendi isteğimize göre ayarladıktan sonra CTRL ve X tuşuna aynı anda basın ve size kayıt edip etmiceğiniz hakkında soru sorucak Y yazın ve enter tuşuna basın.&#x20;

Ardından Değişikliklerin etkili olabilmesi için WSL kapatıp tekrar açmanız gerekmekte.

{% hint style="info" %}
WSL'yi kapatmak için windows terminalizi açınız ve aşağıdaki komutu yazınız.

```
wsl --shutdown
```

Tekrar distronuzu açtığınızda zaten otomatik aktif olacaktır.
{% endhint %}





