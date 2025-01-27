#!/bin/bash

# Based on original PKGBUILD generated by pipman
# Python package author, Dmitry Orlov <me@mosquito.su> <me@mosquito.su>

# Disable various shellcheck rules that produce false positives in this file.
# Repository rules should be added to the .shellcheckrc file located in the
# repository root directory, see https://github.com/koalaman/shellcheck/wiki
# and https://archiv8.github.io for further information.
# shellcheck disable=SC2034,SC2154
# [ToDo]: Add files: User documentation
# [ToDo]: Add files: Tooling
# [FixMe]: Namcap warnings and errors

# Maintainer: Ross Clark <archiv8@artisteducator.com>
# Contributor: Ross Clark <archiv8@artisteducator.com>

_prefix="python"
_relname="cysystemd"

pkgname=${_prefix}-${_relname}
pkgver=1.5.2
pkgrel=2
pkgdesc="A SystemD wrapper on Cython"
arch=(
  "x86_64"
)
url="http://github.com/mosquito/cysystemd"
license=(Apache)
depends=(
  "cython"
  "systemd"
)
makedepends=(
  "python"
  "python-pip"
)
source=(
  "https://files.pythonhosted.org/packages/source/${_relname::1}/${_relname}/${_relname}-${pkgver}.tar.gz"
)
sha512sums=(
  "51ce07ad0ce4d765bda89ae67e8eee9e59d246b38b3e3f7f9ee6d8802bba5b2fd67e59921a30f0c37447ebfa0567cdc2f1e846d0035c2b9364ad937483f3d79c"
)

build() {

  cd "$srcdir/${_relname}-${pkgver}"

  python setup.py build

}

package() {

  cd "$srcdir/${_relname}-${pkgver}"

  python setup.py install --root="$pkgdir/" --skip-build --optimize=1

  install -Dm0644 -t "$pkgdir/usr/share/licenses/$pkgname/" LICENSE

}
