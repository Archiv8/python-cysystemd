# PKGBUILD generated by pipman
# Python package author: Dmitry Orlov <me@mosquito.su> <me@mosquito.su>
pkgname=python-cysystemd
pkgver=1.4.5
pkgrel=1
pkgdesc="SystemD wrapper on Cython"
arch=(any)
url="http://github.com/mosquito/cysystemd"
license=(Apache)
depends=("cython")
makedepends=("python" "python-pip")
build() {
  pip install --no-deps --target="cysystemd" cysystemd==$pkgver
}
package() {
  mkdir -p $pkgdir/usr/lib/python3.7/site-packages/
  cp -r $srcdir/cysystemd/* $pkgdir/usr/lib/python3.7/site-packages/
}
