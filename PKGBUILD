# Maintainer: Matthew Krafczyk <krafczyk.matthew@gmail.com>
# Contributor: Matthew Krafczyk <krafczyk.matthew@gmail.com>

pkgname=ArgParse
pkgver=0.8.2.0.g0ff6f17
pkgrel=1
pkgdesc="ArgParse is a library which emulates the argparse python library"
url="https://github.com/krafczyk/ArgParse"
arch=('x86_64')
license=('GPL')
makedepends=('git' 'cmake')
conflicts=('ArgParse')
provides=('ArgParse')
source=('git://github.com/krafczyk/ArgParse.git#branch=master')
md5sums=('SKIP')

pkgver() {
  cd "$srcdir"/"$pkgname"
  git describe --long --tags | sed 's|^v||;s|-|.|g'
}

build() {
  cd "$srcdir"/"$pkgname"
  cmake -DFINAL_INSTALL_PREFIX=/usr -DCMAKE_INSTALL_PREFIX=${pkgdir}/usr
  make

}

package() {
  cd "$srcdir"/"$pkgname"
  make install
}
