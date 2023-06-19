---
description: temel winget komutları
---

# 🗳 winget kullanımı

## Winget Nedir?

Windows Paket Yöneticisi, Microsoft tarafından Windows 10 ve Windows 11 için tasarlanmış ücretsiz ve açık kaynaklı bir paket yöneticisidir. Bir komut satırı yardımcı programı ve uygulamaları yüklemek için bir dizi hizmetten oluşur. ISV'ler bunu yazılım paketleri için bir dağıtım kanalı olarak kullanabilirler. [Wikipedia (İngilizce)](https://en.wikipedia.org/wiki/Windows\_Package\_Manager)

Anlatılabilcek en kısa yol linux paket yöneticileri gibi bir paket yöneticisidir.

## Paket Nasıl ararım?

search sonra aramak istediğiniz paket ismini yazmalısınız. Örneğin aşağıdaki komuta bakınız.

```
winget search Steam
```

![](<../../.gitbook/assets/image (68).png>)

### Aradığım Paket iki kelimeden oluşuyor nasıl yazmalıyım?

tırnak işareti eklemelisiniz. Örneğin aşağıdaki komuta bakınız.

```
winget search "Visual Studio"
```

![](<../../.gitbook/assets/image (228).png>)

## Paket nasıl yüklerim?



ilk önce search ile arama yaptığınız paketin kimliğini alın neden kimliğini almalıyım derseniz kimlik almadan yapmaya çalışırsanız. İstemediğiniz bir paketi yüklemek zorunda kalırsınız.



Kimliği aldıktan sonra. install sonra --id parametresi ekleyip belirtmelisiniz. Örneği aşağıdan bakabilirsiniz

```
winget install --id Valve.Steam
```

## Paket Nasıl Kaldırırım?

Kimlik bilgisini biliyorsanız tek atma şansınız var bilmiyor iseniz işiniz biraz daha zor normal program kaldırdımız yerdende kaldırabilirsiniz.

Kimliğini biliyorsanız uygulamanın

```
winget uninstall --id Valve.Steam
```

Bilmiyor iseniz ise --id silip uygulamanın ismini yazınız.
