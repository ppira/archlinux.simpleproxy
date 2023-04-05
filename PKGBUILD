# Maintainer: Patrik Pira <papira@flutter.se>

pkgname=simpleproxy
pkgver=3.5+3+g2328a3c
pkgrel=1
pkgdesc='simple tcp proxy'
url="https://github.com/vzaliva/simpleproxy/"
license=(GPL3)
arch=('x86_64')
depends=()
makedepends=()
source=(git+https://github.com/vzaliva/simpleproxy.git)
sha256sums=('SKIP')

pkgver() {
  cd $pkgname
  git describe --tags | sed 's/^v\.//;s/-/+/g'
}

build() {
  cd "$pkgname"
  ./configure --prefix=/usr --mandir=/usr/share/man
  make
}

package() {
  cd "$pkgname"
  make DESTDIR="$pkgdir/" install
}
