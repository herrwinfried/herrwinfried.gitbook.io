---
description: >-
  Linux için Windows Alt Sistemi, Linux ikili yürütülebilir dosyalarını Windows
  10, Windows 11 ve Windows Server 2019'da yerel olarak çalıştırmak için bir
  uyumluluk katmanıdır. Mayıs 2019'da, Hyper-V öz
---

# 🐧 WSL (Microsoft Store)

[Wikipedia alıntılanmıştır.](https://en.wikipedia.org/wiki/Windows\_Subsystem\_for\_Linux)

Google Çeviri ile çevrilmiştir.

#### WSL 2

Sürüm 2, mimarideki değişiklikleri tanıtır. Microsoft, çekirdeği ve dağıtımları (çekirdeğe dayalı olarak) çalıştırmak için yüksek düzeyde optimize edilmiş bir Hyper-V özellikleri alt kümesi aracılığıyla sanallaştırmayı seçti ve WSL 1'e eşdeğer performans vaat ediyor. [Geriye dönük uyumluluk için](https://en.wikipedia.org/wiki/Backward\_compatibility) geliştiricilerin hiçbir şeyi değiştirmesine gerek yok. yayınlanan dağıtımlarında. WSL 2 ayarları , [Kullanıcı Profili klasöründe](https://en.wikipedia.org/wiki/Special\_folder) adı verilen bir [INI dosyasında](https://en.wikipedia.org/wiki/INI\_file) bulunan _WSL genel yapılandırması_ tarafından değiştirilebilir . [\[49\] ](https://en.wikipedia.org/wiki/Windows\_Subsystem\_for\_Linux#cite\_note-Loewen,\_Microsoft\_devblog,\_2019-49)[\[50\]](https://en.wikipedia.org/wiki/Windows\_Subsystem\_for\_Linux#cite\_note-Hillis,\_GitHub,\_2019-50)`.wslconfig`

İç dağıtım tesisatı bulunduğu [ext4](https://en.wikipedia.org/wiki/Ext4) bir iç dosya sistemini -dosyaları biçimlendirilmiş [sanal diske](https://en.wikipedia.org/wiki/Virtual\_disk) ve konak dosya sistemi üzerinden şeffaf erişilebilir [9P protokolü](https://en.wikipedia.org/wiki/9P\_\(protocol\)) , [\[51\]](https://en.wikipedia.org/wiki/Windows\_Subsystem\_for\_Linux#cite\_note-51) gibi diğer sanal makine teknolojilerine benzer [QEMU](https://en.wikipedia.org/wiki/QEMU) . [\[52\]](https://en.wikipedia.org/wiki/Windows\_Subsystem\_for\_Linux#cite\_note-52) Kullanıcılar için Microsoft, WSL 1'in okuma/yazma performansının 20 katına kadar söz verdi. [\[53\]](https://en.wikipedia.org/wiki/Windows\_Subsystem\_for\_Linux#cite\_note-53) Windows'tan , UNC yolu öneki kullanılarak Linux konuk dosyası erişimi için bir [IFS ](https://en.wikipedia.org/wiki/Installable\_File\_System)[ağ yeniden yönlendiricisi](https://en.wikipedia.org/wiki/Network\_redirector) sağlanır `\\wsl$`.

WSL 2, x64 sistemleri için Windows 10 sürüm 1903 veya üzeri, Build 18362 veya üzeri ve ARM64 sistemleri için Build 19041 veya üzeri Sürüm 2004 veya üzeri gerektirir. [\[54\]](https://en.wikipedia.org/wiki/Windows\_Subsystem\_for\_Linux#cite\_note-54)

#### WSLg

WSLg, tam entegre bir masaüstü deneyiminde Windows üzerinde Linux GUI uygulamalarının (X11 ve Wayland) çalıştırılmasına yönelik destek sağlamak amacıyla _oluşturulmuş Linux GUI_ için _Windows Alt_ Sistemi'nin kısaltmasıdır . [\[55\]](https://en.wikipedia.org/wiki/Windows\_Subsystem\_for\_Linux#cite\_note-:1-55) WSLg, [Microsoft Build 2021](https://en.wikipedia.org/wiki/Microsoft\_Build\_2021) konferansında resmi olarak yayınlandı . Windows 10 Insider build 21364 veya sonraki sürümlerde bulunur. [\[31\]](https://en.wikipedia.org/wiki/Windows\_Subsystem\_for\_Linux#cite\_note-:0-31) Bununla birlikte, [Windows 11'in](https://en.wikipedia.org/wiki/Windows\_11) piyasaya sürülmesiyle birlikte WSLg, WSL uygulamalarında hem grafik hem de ses için destek getiren bir Windows üretim yapısıyla nihayet geliyor. [\[56\]](https://en.wikipedia.org/wiki/Windows\_Subsystem\_for\_Linux#cite\_note-56)

**WSLg'yi çalıştırmak için ön koşullar**

* Windows 11 (derleme 22000.\*) veya Windows 11 Insider Preview (21362+ derlemeleri) [\[55\]](https://en.wikipedia.org/wiki/Windows\_Subsystem\_for\_Linux#cite\_note-:1-55)
* WSLg'yi sanal GPU'nun (vGPU) WSL için etkinleştirildiği bir sistemde çalıştırın (İsteğe bağlı, ancak donanım hızlandırmalı OpenGL oluşturmadan yararlanmanıza olanak tanır) [\[55\]](https://en.wikipedia.org/wiki/Windows\_Subsystem\_for\_Linux#cite\_note-:1-55)

[Wikipedia alıntılanmıştır.](https://en.wikipedia.org/wiki/Windows\_Subsystem\_for\_Linux)
