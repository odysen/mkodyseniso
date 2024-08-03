pkgname=mkodyseniso
pkgver="1"
pkgdesc="Patched mkarchiso to build OdysenISO bootable images"
pkgrel=1
pkgdesc="Mkodysen iso"
arch=("x86_64")
license=("GPL3")
depends=("archiso")
url="https://github.com/odysen/mkodyseniso"

prepare() {
    git clone https://gitlab.archlinux.org/archlinux/archiso
    mv archiso/archiso/mkarchiso mkarchiso
    rm -rf archiso
}

build() {
    patch mkarchiso mkodyseniso.patch
    mv mkarchiso mkodyseniso
}

package() {
    install -D mkodyseniso /usr/bin/mkodyseniso
}