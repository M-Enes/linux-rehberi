# Arch Linux Kurulumu

Öncelikle, https://www.technopat.net/sosyal/konu/arch-linux-kurulumu.918194/ buradaki adımları takip edin.

Arch Linux, paket indirme ve kaldırma gibi işlemler için **pacman** isimli paket yöneticisini kullanır.
**pacman** ile işlem yapmadan önce lütfen en son repo bilgileri güncellemelerini aldığınızdan emin olun.
Repo bilgilerini güncellemek için `sudo pacman -Syu` komutunu kullanabilirsiniz.
**pacman** kullanırken komutların başına `sudo` yazmamızın sebebi pacman paket yöneticisinin root izinleri ile çalışmasıdır.

Eğer pacman paket yöneticisi ile yazılım kurarken bir grafik arayüz üzerinden işlem yapmak isterseniz **pamac** isimli paketi kurarak **pamac** yazılımı üzerinden işlemlerinizi yapabilirsiniz.

Ayrıca **pacman** için yazılmış yardımcı uygulamaları kullanarak da paket yönetiminizi daha kolay hale getirebilirsiniz. Örneğin **yay** veya **paru**. **yaourt** kullanmanızı tavsiye etmem çünkü **yaourt** artık geliştirilmiyor.

## Gerekli birkaç kurulum

Ses işlemleri için alsa ve pulseaudio paketlerini pacman yardımıyla kuralım

`sudo pacman -S alsa-lib alsa-utils pulseaudio`

bunlara ek olarak isterseniz pavucontrol yardımıyla grafik arayüzlü olarak kullanabilirsiniz pavucontrol kurulumu için

`sudo pacman -S pavucontrol`

Ardından Timeshift yedekleme yazılımını kurabilirsiniz. (isteğe bağlı)

`sudo pacman -S timeshift`

Emojiler görünmüyorsa `noto-fonts-emoji` isimli paketi kurunuz.

Android cihaz içindeki dosyaları algılamıyorsa `mtpfs` ve `gvfs-mtp` kurunuz. 
Eğer çalışmazsa telefonunuzun android sürümü yeni olabilir. Bunun için ayrıca `jmtpfs` paketini kurunuz.

## Masaüstü Ortamı Kurulumu

Masaüstü ortamı kurmak için öncelikle kullanmak istediğiniz masaüstü  ortamını belirleyiniz.

Sonrasında https://www.technopat.net/sosyal/konu/arch-linux-kurulumu.918194/ adresindeki adımları izleyebilirsiniz.

Orada anlatılmayan masaüstü ortamları için https://wiki.archlinux.org adresine bakınız.

## Sıklıkla kullanılan pacman komutları

`sudo pacman -S {paketismi}` paketi kurmanızı sağlar. (Synchronization)

`sudo pacman -R {paketismi}` paketi kaldırmanızı sağlar. Yalnızca paketi kaldırır. Bağımlı olduğu diğer paketleri kaldırmaz.

`sudo pacman -Rs {paketismi}` paketi ve paketi kurarken yüklediğiniz paketin bağımlı olduğu paketlerden artık kullanılmayanları kaldırır.

`sudo pacman -Rcns {paketismi}` paketi ve tüm bağımlı olduğu paketleri kaldırır. Gerekli olan paketleri de kaldırabileceğinden tavsiye edilmez.

## Sıklıkla kullanılan yay komutları

`yay {paketismi}` ilgili paketleri numaralanmış şekilde listeler, istediğiniz paketin numarasını yazarak indirme yapabilirsiniz.

`yay -S {paketismi}` paketi kurmanızı sağlar.

`yay -R {paketismi}` paketi kaldırma komutudur. Sadece paketi kaldırır. Bağımlı olduğu diğer paketleri kaldırmaz.

`yay -Rns {paketismi}` paketi ve paketi kurarken yüklediğiniz paketin bağımlı olduğu paketlerden artık kullanılmayanları kaldırır.

`yay -Yc` başka bir paket tarafından kendisine gerek duyulmayan gereksiz paketleri kaldırır.
