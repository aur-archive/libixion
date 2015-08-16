# Maintainer: kusakata <shohei atmark kusakata period com>

pkgname=libixion
pkgver=0.7.0
pkgrel=1
pkgdesc="A general purpose formula parser & interpreter"
arch=('i686' 'x86_64')
url="https://gitorious.org/ixion/pages/Home"
license=('MPL2')
makedepends=('boost' 'mdds')
depends=('boost-libs')
options=('!libtool')
source=("http://kohei.us/files/ixion/src/libixion-${pkgver}.tar.bz2")

build() {
	cd "${srcdir}/libixion-${pkgver}"
	./configure --prefix=/usr
	make
}

package() {
	cd "${srcdir}/libixion-${pkgver}"
	make DESTDIR="${pkgdir}" install
	
	install -Dm644 COPYING "${pkgdir}/usr/share/licenses/${pkgname}/COPYING"
}

md5sums=('000157117801f9507f34b26ba998c4d1')
