# Maintainer: Gemini CLI
pkgbase=adwaita-qt-catppuccin-mocha
pkgname=(adwaita-qt5-catppuccin-mocha adwaita-qt6-catppuccin-mocha)
pkgver=1.4.50
pkgrel=2
pkgdesc='A style to bend Qt applications to look like they belong into GNOME Shell (Catppuccin Mocha edition)'
arch=(x86_64)
url='https://github.com/codegod100/adwaita-qt'
license=(GPL)
source=("https://github.com/codegod100/adwaita-qt/releases/download/v$pkgver/adwaita-qt5.so"
        "https://github.com/codegod100/adwaita-qt/releases/download/v$pkgver/libadwaitaqt5.so.1"
        "https://github.com/codegod100/adwaita-qt/releases/download/v$pkgver/libadwaitaqtpriv5.so.1"
        "https://github.com/codegod100/adwaita-qt/releases/download/v$pkgver/adwaita-qt6.so"
        "https://github.com/codegod100/adwaita-qt/releases/download/v$pkgver/libadwaitaqt6.so.1"
        "https://github.com/codegod100/adwaita-qt/releases/download/v$pkgver/libadwaitaqt6priv.so.1")
sha256sums=('SKIP' 'SKIP' 'SKIP' 'SKIP' 'SKIP' 'SKIP')

package_adwaita-qt5-catppuccin-mocha() {
  pkgdesc='A style to bend Qt5 applications to look like they belong into GNOME Shell (Catppuccin Mocha edition)'
  provides=(adwaita-qt5 adwaita-qt)
  conflicts=(adwaita-qt5 adwaita-qt)

  install -Dm755 adwaita-qt5.so "$pkgdir/usr/lib/qt/plugins/styles/adwaita.so"
  install -Dm755 libadwaitaqt5.so.1 "$pkgdir/usr/lib/libadwaitaqt.so.1"
  install -Dm755 libadwaitaqtpriv5.so.1 "$pkgdir/usr/lib/libadwaitaqtpriv.so.1"
  ln -s libadwaitaqt.so.1 "$pkgdir/usr/lib/libadwaitaqt.so"
  ln -s libadwaitaqtpriv.so.1 "$pkgdir/usr/lib/libadwaitaqtpriv.so"
}

package_adwaita-qt6-catppuccin-mocha() {
  pkgdesc='A style to bend Qt6 applications to look like they belong into GNOME Shell (Catppuccin Mocha edition)'
  provides=(adwaita-qt6)
  conflicts=(adwaita-qt6)

  install -Dm755 adwaita-qt6.so "$pkgdir/usr/lib/qt6/plugins/styles/adwaita.so"
  install -Dm755 libadwaitaqt6.so.1 "$pkgdir/usr/lib/libadwaitaqt6.so.1"
  install -Dm755 libadwaitaqt6priv.so.1 "$pkgdir/usr/lib/libadwaitaqt6priv.so.1"
  ln -s libadwaitaqt6.so.1 "$pkgdir/usr/lib/libadwaitaqt6.so"
  ln -s libadwaitaqt6priv.so.1 "$pkgdir/usr/lib/libadwaitaqt6priv.so"
}
