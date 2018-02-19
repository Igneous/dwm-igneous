pkgname=dwm-igneous
pkgver='6.1.r2.u_6aa8e37.f_064ea90'
pkgrel=1
pkgdesc="A dynamic window manager for X"
url="http://dwm.suckless.org"
arch=('i686' 'x86_64')
license=('MIT')
options=(zipman)
depends=('libx11' 'libxinerama' 'libxft' 'freetype2' 'st' 'dmenu' 'clang')
source=(config.h drw.h util.h drw.c dwm.c transient.c util.c dwm.1 Makefile config.mk config.def.h LICENSE README)

build() {
  cd "$srcdir"
  make CC=clang
}

package() {
  cd "$srcdir"
  make PREFIX=/usr DESTDIR="$pkgdir" install
  install -m644 -D LICENSE "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
  install -m644 -D README "$pkgdir"/usr/share/doc/$pkgname/README
}

md5sums=('0ca6ad0588363e75a35134bbf75e1026'
         'c6dd16edfb2893a4295a11f655dcb629'
         '007c065ca60e3f3c56bf153f2f769a90'
         'd2503d33395c959349fea754b0cff191'
         'bc922b468045149f9d8c350aa23e1562'
         '1f002e4c3da39eed17c5581e8649daa1'
         'e1d877b57636568ba579b1bc0ae42e8f'
         '6356eb6e663c273b6bc8e00cdd3799ef'
         '62489d2f9bdd33597d34ed2b8c85f1cf'
         'f078fe82eade645ffa91282006a68fa9'
         'a58b803f96ea731c9e0c60e088a72864'
         '8555b535ebdcbd0f153d5c9fabde7168'
         '071f8af116f50e3d6b7ea0ab39b343d0')
