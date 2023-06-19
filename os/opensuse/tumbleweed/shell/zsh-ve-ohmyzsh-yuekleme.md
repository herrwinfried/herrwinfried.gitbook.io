---
description: OpenSUSE Tumbleweed ZSH ve OhMyZsh kurulumu hakkında rehber
---

# ZSH ve OhMyZsh Yükleme

{% hint style="warning" %}
Bu rehber sırasında terminal kullanılacaktır.
{% endhint %}

## 1.Adım: Zsh Yükleme

Aşağıdaki Komutu terminale yazalım.

```bash
sudo zypper in -y zsh git curl
```

{% hint style="info" %}
DNF ile yüklemek isterseniz

{% code overflow="wrap" %}
```bash
sudo dnf install -y zsh git curl
```
{% endcode %}
{% endhint %}

## 2. Adım OhMyZSH Yükleme

Aşağıdaki Komutu terminale yazalım.

```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

yükleme işlemi bittiğinde size varsayınal olarak ayarlanmasını istediğiniz sorucak eğer istiyor iseniz sadece "y" istemiyorsanız sadece "n" yazmalısınız. Eğer varsayınal olarak ayarlamasını isterseniz sizden ardından parolanızı isteyecektir parolanızı girdikten sonra işlem tamamlanmış olacaktır. Eğer hala bash geliyorsa varsayınal seçtiğinizde oturumu kapatıp tekrar giriniz.

## BONUS: Powerline10k Nasıl Yüklenir?

{% hint style="warning" %}
Zsh ve OhMyZSH yüklü olması gerekmektedir.
{% endhint %}

Aşağıdaki komutları girelim.

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

```bash
powerline10xx=$(cat ~/.zshrc | grep -v "#" | grep -m1 ZSH_THEME)
```

{% hint style="danger" %}
Yöntem deneyseldir sorumluluk almıyorum eğer dosyaların bozulcağı şüphen olursa gedit, kate gibi editorler ile açmayı deneyebilirsin.

`gedit ~/.zshrc`

ZSH\_THEME içindeki değeri değiştir ve aşağıda görünen gibi yap!

```bash
ZSH_THEME="powerlevel10k/powerlevel10k"
```
{% endhint %}

```bash
sed -ie 's+'$powerline10xx'+ZSH_THEME="powerlevel10k/powerlevel10k"+i' ~/.zshrc
```

{% hint style="info" %}
Root tarafı içinde aynı işlemi yapmanız gerekir. Daha doğru bir tanım kullanmak istersek mevcut oturumdaki üzerinde değişiklik yapmaktadır.
{% endhint %}
