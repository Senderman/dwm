# Maintainer: Fyodor Doletov <doletov.fyodor@yandex.ru>

pkgname=dwm-senderman-edition-git
pkgver=6.4
pkgrel=8
pkgdesc="A dynamic window manager for X, patched by Senderman"
url="https://github.com/Senderman/dwm"
arch=('i686' 'x86_64')
license=('MIT')
options=(zipman)
depends=('libx11' 'libxinerama' 'libxft' 'polybar-dwm-git' 'ttf-material-design-icons-webfont' 'yajl')
makedepends=('git')
provides=('dwm')
conflicts=('dwm')
source=(
  config.def.h
  config.mk
  drw.c
  drw.h
  dwindle.c
  dwm.1
  dwm.c
  dwm-msg.c
  dwm.png
  grid.c
  ipc.c
  IPCClient.c
  IPCClient.h
  ipc.h
  LICENSE
  Makefile
  README
  transient.c
  util.c
  util.h
  yajl_dumps.c
  yajl_dumps.h
)
sha256sums=('44a6ed5feb17a4f83c4f717698c6e43d26bba4852fd5aaa06c7e794f9f9abea6'
            '330f2c23ddd59b9827c79951d9e03732b0b8fc16c2d20362101ea88bb0d015e5'
            '8efce2f953bf82de30c975a2ddbd13d54fdf00aedbd4572bf9292cd2f64e9b93'
            'b4a6864eb2c2e3f320bd4d2ac37a9bb53435911e115a17f7a2a3b698a9dbd228'
            '6da7aaa324a204832bc43ada0221051148f067fcd72abced3309ea20c73213f6'
            'e97f42257c05b7298a15a57c5a579b534ab37a305fc3bdc6f2c9d04788f3ab51'
            '94f0acb4228923cd070353abfa5eff0d5f59e6f756994633d5ba2ecbd27fac52'
            '93c825a85cf585677d1582cd5048f1fffbf18792a1fb941f27c325275eaa91e9'
            'b608fe5d3e221f8867f5d3c7907071d31145b04ff96bfe08c734fede02e2ff38'
            'a7ad319e77505c2b8e4cae56b8eb1586eb46e8f9e581e74229ee6cfb06bcfdc3'
            '0074fca9ca7fcbfdab64829f0b064dc62547c1932fd53563badbefddbc6b016f'
            '6974268c6dd3273abfffe3c77cc950059f9d2a5b3d56d3e2c92b12d5fb97543d'
            '9f47bcedb0f35e02a6dde20d5282768b6d4040f751466b44d6ee54c8c57ad7da'
            '9f333c6cd45961c826884537bd4e8bbfe88f899d377aa62b1ad3d7b14f641267'
            '8bbe268a549563fb2895eefd3c43869ca436eda0ba826474334270ad84a7c98d'
            '7c59b168f7004fbfdf5f1c8b2a21cb8c89a96ec66d81e980cc6a7ddc338c05cf'
            'f0384e29e3f249fcd52a30c35c722fca50e9fabfdeb7725f4073e05170358d86'
            '54c37c558613ab3da856b19c4b4c0c56c224133a253bf5fa6557b489da545d7c'
            '0682ab1c066141f48e215760dd20148c79856f247ee22584de5a31e5f50310da'
            '5b1ff1d8dca72ec0a73adceba74b4382f31521c53068f2afcae724d56dd44ece'
            '7fca14398ca3aed460c6207b710a8b85f0b8556100bbffd6de97b8d4b483a80f'
            '1470c7a9e1f183eb61f010939e7a4b8e4ca7cdd9a6d457a25c150aa454ab0fce')

build() {
  make X11INC=/usr/include/X11 X11LIB=/usr/lib/X11
}

package() {
  make PREFIX=/usr DESTDIR="$pkgdir" install
  install -m644 -D LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
  install -m644 -D README "$pkgdir/usr/share/doc/$pkgname/README"
}


