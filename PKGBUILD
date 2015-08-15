# Maintainer: nosada <ngsksdt@gmail.com>

pkgname=conoha-ojs
pkgver=20150406.1
pkgrel=1
pkgdesc="CLI-tool for ConoHa Object Storage"
arch=("x86_64")
url="https://github.com/hironobu-s/conoha-ojs"
_gouri="github.com/hironobu-s/conoha-ojs"
license=("MIT")
depends=("go")
makedepends=("mercurial")

build() {
  GOPATH=${srcdir} go get ${_gouri}
  cd ${srcdir}/src/${_gouri}
  GOPATH=${srcdir} make linux
}

package() {
  mkdir -p ${pkgdir}/usr/bin
  install -p -m755 ${srcdir}/src/${_gouri}/bin/linux/${pkgname}  ${pkgdir}/usr/bin/${pkgname}
}

# vim:set ts=2 sw=2 et:
