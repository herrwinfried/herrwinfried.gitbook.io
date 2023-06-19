---
description: WSL (MS Store) windows PATH devre dışı bırakma hakkında bahsettiğim rehberim.
---

# 🗃 Windows PATH devre dışı bırakma

{% hint style="warning" %}
Bu işlemi yaparken WSL dağıtımınızdan yapmalısınız. Genel WSL konfigürasyon ayarlarında çalışmamaktadır.
{% endhint %}

{% hint style="info" %}
Bu rehberde nano editorü üzerinden anlatılmaktadır isterseniz gedit vb. editorler kullanabilirsiniz.
{% endhint %}

WSL dağıtımımızı açtıktan sonra terminale aşağıdaki komutu yazıyoruz.

```
sudo nano /etc/wsl.conf
```

ardından parolamızı girip enter basıyoruz daha sonra aşağıdaki gibi yazıyoruz.

```
[interop]
appendWindowsPath=false
```

ardından `CTRL+X` basıp y yazıyoruz ve enter basıyoruz daha sonra windows powershell dönüp&#x20;

```
wsl --shutdown
```

yazıyoruz ve tekrar açtığımızda artık Windows PATHleri yok.
