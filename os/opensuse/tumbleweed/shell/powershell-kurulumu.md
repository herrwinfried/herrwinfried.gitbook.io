---
description: OpenSUSE Tumbleweed Powershell kurulumu hakkında rehber
---

# Powershell Kurulumu

{% hint style="info" %}
Powershell openSUSE için direkt olarak bir rpm dosyası sunmadığı için kendimiz terminale yazmamız gerekiyor.
{% endhint %}

İlk önce gerekli bağımlılıkları kurmamız gerekiyor.

```bash
sudo zypper dup -y
```

{% code overflow="wrap" %}
```bash
sudo zypper in -y curl tar jq && sudo zypper in -y libicu60_2 && sudo zypper in -y libopenssl1_0_0 
```
{% endcode %}

{% hint style="info" %}
DNF ile yüklemek isterseniz

{% code overflow="wrap" %}
```bash
sudo dnf refresh && sudo dnf install -y curl tar jq && sudo dnf install -y libicu60_2 && sudo dnf install -y libopenssl1_0_0 
```
{% endcode %}
{% endhint %}

Sırasıyla yukardaki komutları yazalım. Ardından Kuruluma geçebiliriz.

Şimdi aşağıdaki işlemleri tek tek yapalım.

```bash
pwshcore=$(curl -s https://api.github.com/repos/PowerShell/PowerShell/releases/latest| jq -r ".assets[] | select(.name | test(\"linux-x64.tar.gz\")) | .browser_download_url")
```

```bash
curl -L $pwshcore -o /tmp/powershell.tar.gz
```

<pre class="language-bash"><code class="lang-bash"><strong>sudo mkdir -p /opt/microsoft &#x26;&#x26; sudo mkdir -p /opt/microsoft/powershell
</strong></code></pre>

```bash
sudo tar -xzf /tmp/powershell.tar.gz -C /opt/microsoft/powershell/
```

```bash
sudo ln -s /opt/microsoft/powershell/pwsh /usr/bin/pwsh
```

```bash
sudo chmod +x /usr/bin/pwsh
```

herşey yolunda gitti ise başarıyla kurulumu gerçekleştirmişsiniz demektir! Kodumuzu açıklamız gerekir ise ilk önce GitHub API kullanarak son yayınlanan sürüm öğreniyoruz daha sonra jq ile bu değeri netleştiriyoruz. Ardından Curl komutu kullanıp /tmp dizine indiriyoruz. Ardından opt klasörün içinde microsoft içinde powershell klasörü oluşturuyoruz. Ardından indirdiğimiz powershell oraya taşıyoruz ardından usr/bin powershell bir sembolik link olarak bırakıyoruz ve son olarak çalıştırma izni tanımlıyoruz. Artık Tamam Powershell başarıyla kurmuş olduk! Her güncellemede bunu tekrar yapmamız gerekiyor tek yapmamız gereken /opt/microsoft/powershell dizini boşaltmamız ve öyle yapmamız gerekiyor.

{% hint style="info" %}
/opt/microsoft/powershell klasörünü boşaltmak isterseniz (Hem powershell hemde microsoft klasörü)

`sudo rm -rf /opt/microsoft`

Eğer sadece powershell klasörün içindekileri silmek istersen

`sudo rm -rf /opt/microsoft/powershell/*`
{% endhint %}
