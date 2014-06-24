# Maintainer: Hugo Osvaldo Barrera <hugo@osvaldobarrera.com.ar>

pkgname=bcklight
pkgver=1
pkgrel=1
pkgdesc="A very simple application that changes MacBooks' led backlight level."
arch=("x86_64")
url="https://github.com/brainwave/bcklight/"
license=('BSD')
source=("https://github.com/brainwave/$pkgname/archive/v${pkgver}.zip")
md5sums=('0d5b331f05053f92ccd1e6bc82286234')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir/" PREFIX=/usr/ install
  chmod 4755 "$pkgdir/usr/bin/$pkgname"
}
