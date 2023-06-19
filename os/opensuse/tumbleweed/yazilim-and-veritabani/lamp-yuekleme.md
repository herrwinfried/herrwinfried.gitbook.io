---
description: OpenSUSE Tumbleweed LAMP yükleme hakkında rehber
---

# LAMP Yükleme

{% hint style="warning" %}
Bu rehber sırasında terminal kullanılacaktır.
{% endhint %}

Aşağıdaki Komutları yazalım...

```bash
sudo su
```

## Apache2

### Apache2 Yükleme

```bash
sudo zypper --gpg-auto-import-keys in -y apache2
```

### Apache2 Başlatma

<pre class="language-bash"><code class="lang-bash"><strong>sudo systemctl start apache2
</strong></code></pre>

{% hint style="info" %}
durdurmak için:\
`sudo systemctl stop apache2`

Yeniden başlatmak için:

`sudo systemctl restart apache2`
{% endhint %}

### Güvenlik Duvarı?

Eğer firewalld aktif ise yapmanız gereken port firewall eklemek. Aşağıdaki komut ile kolayca ekliyebilirsin.

```bash
sudo firewall-cmd --zone=public --add-port=80/tcp --permanent && sudo firewall-cmd --reload
```

### Apache2 Test Etmek

`/srv/www/htdocs/` klasörüne index.html dosyası oluşturalım.

```bash
touch /srv/www/htdocs/index.html && echo "<html><body><h1>Welcome to my web site!</h1></body></html>" | tee /srv/www/htdocs/index.html
```

## PHP8 Yükleme

<pre><code><strong>sudo zypper --gpg-auto-import-keys in -y php8 php8-mysql apache2-mod_php8
</strong></code></pre>

### Apache2 Başlatma

<pre class="language-bash"><code class="lang-bash"><strong>sudo systemctl start apache2
</strong></code></pre>

{% hint style="info" %}
durdurmak için:\
`sudo systemctl stop apache2`

Yeniden başlatmak için:

`sudo systemctl restart apache2`
{% endhint %}

### Ayarlamalar

```bash
a2enmod php8
```

```
sudo echo "AddType application/x-httpd-php .php" >> /etc/apache2/mod_mime-defaults.conf
```

## MariaDB & MySQL

### Yükleme

<pre><code><strong>sudo zypper --gpg-auto-import-keys in -y mariadb mariadb-tools
</strong></code></pre>

### MariaDB Başlatma

<pre class="language-bash"><code class="lang-bash"><strong>sudo systemctl start mysql
</strong></code></pre>

{% hint style="info" %}
durdurmak için:\
`sudo systemctl stop` mysql

Yeniden başlatmak için:

`sudo systemctl restart` mysql
{% endhint %}

### Ayarlamalar

```
sudo mysql_secure_installation
```

aşağıdaki gibi soruları yanıtlayın.

{% hint style="info" %}
ingilizce olarak gelceğini düşündüğümden ingilizce bıraktım cevapları
{% endhint %}

* Enter current password for root (enter for none): Just press the <mark style="color:red;">Enter</mark>
* Set root password? \[Y/n]: <mark style="color:red;">Y</mark>
* New password: <mark style="color:red;">Parola girin</mark>
* Re-enter new password: <mark style="color:red;">Parolayı Tekrar Girin</mark>
* Remove anonymous users? \[Y/n]: <mark style="color:red;">Y</mark>
* Disallow root login remotely? \[Y/n]: <mark style="color:red;">Y</mark>
* Remove test database and access to it? \[Y/n]:  <mark style="color:red;">Y</mark>
* Reload privilege tables now? \[Y/n]:  <mark style="color:red;">Y</mark>

{% hint style="success" %}
MYSQL bağlanmak isterseniz.

parolanızı giriniz

```bash
sudo mysql -u root -p
```
{% endhint %}
