# Maintainer: Fyodor Doletov <doletov.fyodor@yandex.ru>

pkgname=dwm-senderman-edition-git
_pkgname=dwm
pkgver=6.4
pkgrel=1
pkgdesc="A dynamic window manager for X, patched by Senderman"
url="https://github.com/Senderman/dwm"
arch=('i686' 'x86_64')
license=('MIT')
options=(zipman)
depends=('libx11' 'libxinerama' 'libxft' 'polybar-dwm-module' 'ttf-material-design-icons-webfont')
makedepends=('git')
provides=('dwm')
conflicts=('dwm')
source=("$_pkgname::git+$url.git")
md5sums=('SKIP')

build() {
  cd $_pkgname
  make X11INC=/usr/include/X11 X11LIB=/usr/lib/X11
}

package() {
  cd $_pkgname
  make PREFIX=/usr DESTDIR="$pkgdir" install
  install -m644 -D LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
  install -m644 -D README "$pkgdir/usr/share/doc/$pkgname/README"
}

# vim:set ts=2 sw=2 et:
