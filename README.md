# Intro

# TO DO
* fichiers de conf
* explications générales sur comment flasher
* présenter les flasher pas cher
* expliquer comment builder une image en général
* faire la procédure de build pour chaque image
* inclure les blobs éventuels (pour e350m1)
* D510MO, D945GCLF blob free
* faire testa globale pour KPGE-D16/128Go avec OpenBMC module et asus PIKE 
* ajouter un PDF fr et en pour expliquer le tout. 
* modifier les README.md des boards avec un tableau

# Petitboot compilation

1 - Install requested packages
```
sudo apt-get install -y bison build-essential curl flex gnat-5 libncurses5-dev m4 zlib1g-devlibtool \
libgcrypt  git lzma busybox petitboot systemd autotools-dev autoconf intltool gperf libcap-dev libblkid-dev \
python-lxml libmount-dev zlib1g-dev uuid-dev libdigest-sha-perl libelf-dev bc bzip2 bison gnupg iasl m4 nasm \
patch python wget cpio ccache pkg-config cmake libusb-1.0-0-dev pkg-config texinfo
```
