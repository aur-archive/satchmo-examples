# Maintainer: Arch Haskell Team <arch-haskell@haskell.org>
_hkgname=satchmo-examples
pkgname=satchmo-examples
pkgver=1.4.1
pkgrel=3
pkgdesc="examples that show how to use satchmo"
url="http://hackage.haskell.org/package/${_hkgname}"
license=('GPL')
arch=('i686' 'x86_64')
makedepends=('ghc' 'haskell-array=0.3.0.1' 'haskell-containers=0.3.0.0' 'haskell-process=1.0.1.3' 'haskell-satchmo>=1.4' 'haskell-satchmo-backends>=1.4' 'haskell-satchmo-funsat>=1.4')
depends=('gmp')
options=('strip')
source=(http://hackage.haskell.org/packages/archive/${_hkgname}/${pkgver}/${_hkgname}-${pkgver}.tar.gz)
build() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup configure --prefix=/usr --docdir=/usr/share/doc/${pkgname} -O
    runhaskell Setup build
}
package() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup copy --destdir=${pkgdir}
}
md5sums=('73721664af9b99461294ac403a6210e2')
