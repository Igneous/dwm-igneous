pkgname=dwm-igneous
pkgver='6.1.r1.u_6aa8e37.f_09ac512'
pkgrel=1
pkgdesc="A dynamic window manager for X"
url="http://dwm.suckless.org"
arch=('i686' 'x86_64')
license=('MIT')
options=(zipman)
depends=('libx11' 'libxinerama' 'libxft' 'freetype2' 'st' 'dmenu' 'clang')

build() {
  make CC=clang
}

package() {
  cd "$srcdir"/$pkgname-$pkgver
  make PREFIX=/usr DESTDIR="$pkgdir" install
  install -m644 -D LICENSE "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
  install -m644 -D README "$pkgdir"/usr/share/doc/$pkgname/README
  install -m644 -D "$srcdir"/dwm.desktop "$pkgdir"/usr/share/xsessions/dwm.desktop
}
