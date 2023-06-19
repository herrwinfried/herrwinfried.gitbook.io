---
description: OpenSUSE Tumbleweed PostreSQL Kurulumu hakkında rehber
---

# PostreSQL Kurulumu

{% hint style="warning" %}
Bu rehber sırasında terminal kullanılacaktır.
{% endhint %}

{% hint style="info" %}
Güvenlik duvarı bu rehberimizde varsayınal olarak kapalı sayılacaktır.
{% endhint %}

## PostreSQL Yükleme

### PostreSQL Deposunu Ekleme

Lütfen terminale aşağıdaki komutları sırasıyla yazınız.

```bash
sudo zypper --non-interactive --quiet addrepo --refresh -p 90  http://download.opensuse.org/repositories/server:database:postgresql/openSUSE_Tumbleweed/ PostgreSQL
```

Depomuzdaki paketlerin güncelliğinden emin olmak için aşağıdaki komutu yazalım.

```bash
sudo zypper --gpg-auto-import-keys ref
```

### PostreSQL Yükleme

Aşağıdaki komutu yazalım.

```bash
sudo zypper --gpg-auto-import-keys in -y postgresql postgresql-server postgresql-contrib
```

### Ayarlamalar

{% hint style="success" %}
Bu kısımda anlatılcak olanlar localhost(127.0.0.1) içindir.
{% endhint %}

{% hint style="warning" %}
Genellikle varsayınal Konum `/var/lib/pgsql/data` olmaktadır.&#x20;



Bulamıyor musun?

```bash
sudo find / -name postgresql.conf
```
{% endhint %}

{% hint style="info" %}
nano yerine başka editorlerde tercih edebilirsiniz gedit kwrite kate vb..
{% endhint %}

Aşağıdaki komutları sırasıyla yazınız.

```bash
sudo su
```

```bash
cd /var/lib/pgsql/data
```

```bash
nano postgresql.conf
```

Aşağıdaki resimdeki gibi işaretlenen değerlerin başındaki `#` işaretini kaldırınız listen\_Addresses = '\*' değil ise düzeltin ve görseldeki gibi yapınız.

<figure><img src="../../../../.gitbook/assets/image (140).png" alt=""><figcaption></figcaption></figure>

ardından CTRL + X basıp Y yazıp enter tuşuna basınız.&#x20;

```bash
nano pg_hba.conf
```

{% hint style="danger" %}
Eklenecek IP değerleri Local için bile tehlikeli olabilir. Lütfen Sadece Local üzerinden çalışcaksa aşağıdaki IP'leri yazınız server için kullancaksanız lütfen daha farklı şekilde konfigurasyon yapınız.
{% endhint %}

Aşağıdaki resimde gösterilen yerin altına şu değerleri ekleyiniz

```bash
host    all             all             127.0.0.1/32            md5
host    all             all             ::1/128                 md5
```

<figure><img src="../../../../.gitbook/assets/image (125).png" alt=""><figcaption></figcaption></figure>

ardından CTRL + X basıp Y yazıp enter tuşuna basınız.&#x20;

### Bilgilendirme

#### PostreSQL Başlatma

```bash
sudo systemctl start postgresql
```

#### Eğer sistemi her açtığınızda başlamasını isterseniz

<pre class="language-bash"><code class="lang-bash"><strong>sudo systemctl enable postgresql
</strong></code></pre>

