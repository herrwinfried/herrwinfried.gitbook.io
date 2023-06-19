---
description: >-
  WSL (MS Store) Nasıl CPU ve ram kullanım oranları değiştirilir bundan
  bahsediyorum
---

# ❓ WSL CPU ve Ram kullanım oranını değiştirme

## Sistem Genelinde Değiştirme

Bir Not defteri açınız. Ve aşağıdakileri yazınız

{% hint style="info" %}
Kendi gereksimlerinize göre güncelleyin. #'den sonrasını yazmayabilirsiniz. memory hazıfa/ram demektir. processors ise CPU/İşlemcinin çekirdek sayısıdır.
{% endhint %}

```
[wsl2]
memory=12GB   # WSL 2'deki VM belleğini 12 GB'a kadar sınırlar
processors=4 # WSL 2'deki VM İşlemcisini 4 çekirdek ile sınırlar
```

kendi isteğimize göre ayarladıktan sonra&#x20;

Dosya > Farklı Kaydet diyoruz

ardından C:\Users\\\<Kullanıcı>\ klasörüne gidiyoruz ve .wslconfig olarak dosyamızı kayıt ediyoruz.

![](<../.gitbook/assets/image (82).png>)

Ardından WSL açık ise yeni değişikliklerimizi uygulaması adına kapatıyoruz.

{% hint style="info" %}
WSL'yi kapatmak için windows terminalizi açınız ve aşağıdaki komutu yazınız.

```
wsl --shutdown
```

Tekrar distronuzu açtığınızda zaten otomatik aktif olacaktır.
{% endhint %}

## Sadece Seçtiğim distroda CPU ve Ram değiştirme

{% hint style="success" %}
Bu Yöntemde Metin editörü olarak nano kullanıcağız. Ve Shell kabuk olarak Bash tercih ediceğiz. Siz isterseniz gedit veya başka bir text editor indirip deniyebilirsiniz. Shell olarak kendi tercihinizdekini kullanabilirsiniz.
{% endhint %}

Aşağıdaki Komutu Shell'imize yazalım.

```
sudo nano /etc/wsl.conf
```

yazınız. Ardından metin editörümüz açıldıktan sonra aşağıdakileri yazınız

{% hint style="info" %}
Kendi gereksimlerinize göre güncelleyin. #'den sonrasını yazmayabilirsiniz. memory hazıfa/ram demektir. processors ise CPU/İşlemcinin çekirdek sayısıdır.
{% endhint %}

```
[wsl2]
memory=12GB   # WSL 2'deki VM belleğini 12 GB'a kadar sınırlar
processors=4 # WSL 2'deki VM İşlemcisini 4 çekirdek ile sınırlar
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

