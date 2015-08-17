# Maintainer: Alexey Korobtsov <korobcoff@gmail.com>
pkgname=qtnote
pkgver=3.0.0
pkgrel=1
pkgdesc="Note-taking application written with Qt in mind and able to read tomboy notes"
arch=('i686' 'x86_64')
url="http://ri0n.github.io/QtNote/"
license=('GPL2')
depends=('qt5-base')
conflicts=(QtNote-git)
source=(https://github.com/Ri0n/QtNote/archive/$pkgver.tar.gz)
md5sums=('SKIP') 
_pkgname=QtNote
prepare() {
	cd "$srcdir/$_pkgname-$pkgver"
}

build() {
	cd "$srcdir/$_pkgname-$pkgver"
qmake -recursive CONFIG+=nokde 
make
}


package() {
  cd "$srcdir/$_pkgname-$pkgver"

  make INSTALL_ROOT="$pkgdir" install

}

