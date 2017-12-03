# Maintainer : Shawn Dellysse sdellysse@gmail.com
pkgname=farch
pkgver=0.0.20171203
pkgrel=1
pkgdesc="Functional archlinux system configuration tool"
url="https://github.com/shawndellysse/farch"
arch=("any")
depends=("nodejs")
makedepends=("npm")
source=("https://github.com/shawndellysse/farch/archive/v${pkgver}.tar.gz")
md5sums=('8a4f9b655a9d110902e4956e79c0b2b8')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  npm install --production
}

package() {
  install -dm755 "${pkgdir}/usr/bin"
  install -dm755 "${pkgdir}/usr/share/${pkgname}"


  cd "${srcdir}/${pkgname}-${pkgver}"
  cp -a . "${pkgdir}/usr/share/${pkgname}"

  cd "${pkgdir}/usr/bin"
  ln -sf ../share/${pkgname}/bin/* .
}
