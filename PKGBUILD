# Maintainer: Gemini CLI
pkgbase=adwaita-qt-catppuccin-mocha
pkgname=(adwaita-qt5-catppuccin-mocha adwaita-qt6-catppuccin-mocha)
pkgver=1.4.50
pkgrel=2
pkgdesc='A style to bend Qt applications to look like they belong into GNOME Shell (Catppuccin Mocha edition)'
arch=(x86_64)
url='https://github.com/codegod100/adwaita-qt'
license=(GPL)
makedepends=(cmake qt5-x11extras qt6-base)
source=("git+$url")
sha256sums=('SKIP')

build() {
  cmake -B build-qt5 -S adwaita-qt \
    -DCMAKE_INSTALL_PREFIX=/usr \
    -DUSE_QT6=OFF
  cmake --build build-qt5

  cmake -B build-qt6 -S adwaita-qt \
    -DCMAKE_INSTALL_PREFIX=/usr \
    -DUSE_QT6=ON
  cmake --build build-qt6
}

package_adwaita-qt5-catppuccin-mocha() {
  pkgdesc='A style to bend Qt5 applications to look like they belong into GNOME Shell (Catppuccin Mocha edition)'
  depends=(qt5-x11extras)
  provides=(adwaita-qt5 adwaita-qt)
  conflicts=(adwaita-qt5 adwaita-qt)

  DESTDIR="$pkgdir" cmake --install build-qt5
}

package_adwaita-qt6-catppuccin-mocha() {
  pkgdesc='A style to bend Qt6 applications to look like they belong into GNOME Shell (Catppuccin Mocha edition)'
  depends=(qt6-base)
  provides=(adwaita-qt6)
  conflicts=(adwaita-qt6)

  DESTDIR="$pkgdir" cmake --install build-qt6
}
