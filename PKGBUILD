# Maintainer: Andrzej Giniewicz <gginiu@gmail.com>

pkgname=python2-atom
pkgver=0.3.10
pkgrel=1
pkgdesc="Memory efficient Python objects"
arch=('i686' 'x86_64')
url="https://github.com/nucleic/atom"
depends=('python2')
makedepends=('python2-setuptools')
conflicts=('python2-gdata')
license=('BSD')
options=(!libtool)
source=(https://github.com/nucleic/atom/archive/${pkgver}.tar.gz)
md5sums=('0d4a6464505039218aa60acdde7eef1f')

build() {
  cd "${srcdir}"/atom-${pkgver}

  python2 setup.py build
}

package() {
  cd "${srcdir}"/atom-${pkgver}

  python2 setup.py install --prefix=/usr --root="${pkgdir}" --optimize=1

  install -D COPYING.txt "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

