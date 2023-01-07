# Maintainer: Pompipi <pompipi at outlook dot com>

pkgname=nasm
pkgver=2.16.01
pkgrel=1
pkgdesc='Netwide Assembler (NASM)'
url='https://www.nasm.us'
arch=('x86_64')
license=('MIT')
depends=('glibc')
source=(https://www.nasm.us/pub/nasm/releasebuilds/${pkgver}/${pkgname}-${pkgver}.tar.xz)
sha512sums=('51fccb5639ce019d9c423c0f279750ffbd74c64cd41dd3b185d1aa1a1aaed79c5d3cd8d4bebbc13ee249a375ed27457ea2abde1a4dbb24d354598fffd1254833')
b2sums=('0f7e96648e3db6fa4a8e10a89885f61cab7d79af25adbcc9d4706b3af61206c3cae024b7f873d636f5c1b2cb34ce5e7fbecc16af9b59086e9a1f49fb37c59670')

build() {
  cd ${pkgname}-${pkgver}
  sh configure
  make
}

package() {
  cd ${pkgname}-${pkgver}
  make DESTDIR="${pkgdir}" install
}
