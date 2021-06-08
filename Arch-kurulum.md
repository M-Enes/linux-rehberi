# Arch Linux Kurulumu

Öncelikle, https://www.technopat.net/sosyal/konu/arch-linux-kurulumu.918194/ buradaki adımları takip edin.

Ardından ses işlemleri için alsa ve pulseaudio paketlerini pacman yardımıyla kuralım

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
