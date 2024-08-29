pkgname=mkodyseniso-hc
pkgver="1"
pkgrel="0"
pkgdesc="Patched mkarchiso to build OdysenISO bootable images (home customizer script included)"
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
    patch mkarchiso ../mkodyseniso.patch
    mv mkarchiso mkodyseniso-hc
}

package() {
    install -D mkodyseniso-hc "${pkgdir}/usr/bin/mkodyseniso-hc"
}