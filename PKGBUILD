# Maintainer: scorn <scorn@voidrane.com>
pkgname=kde-splash-creator
pkgver=1.0
pkgrel=1
pkgdesc="A tool for creating custom KDE Plasma splash screens with images, text, and animated elements"
arch=('x86_64')
url="https://github.com/numbpill3d/KDE-SPLASH-CREATOR"
license=('GPL3')
depends=('qt6-base')
makedepends=('cmake' 'git')
source=("git+https://github.com/numbpill3d/KDE-SPLASH-CREATOR.git#tag=v${pkgver}")
sha256sums=('SKIP')

build() {
  cd "${srcdir}/${pkgname}"
  cmake -B build -S . \
    -DCMAKE_INSTALL_PREFIX=/usr \
    -DCMAKE_BUILD_TYPE=Release
  cmake --build build
}

package() {
  cd "${srcdir}/${pkgname}"
  DESTDIR="${pkgdir}" cmake --install build
}