# Contributor: marcus fritzsch <fritschy@googlemail.com>
# Contributor: Xyne
# Contributor: Mrbit

pkgname=easyiso
name=EasyISO
pkgver=0.20
pkgrel=2
pkgdesc="EasyISO helps you manage CD/DVD images , mount them into a specific folder."
url="http://kde-apps.org/content/show.php?content=148840"
license="GPL"
depends=('qt4' )
makedepends=('gcc')
arch=('i686' 'x86_64')
source=("http://kde-apps.org/CONTENT/content-files/148840-$name.tar.bz2")
md5sums=('04201be63acff8ff19474a7f3b8f0ed4')

build() {
  
  sed -i '47 a\#include <unistd.h>/' $srcdir/$name/singleapp/src/qtlocalpeer.cpp
  cd "$srcdir/$name"
  qmake-qt4
  make -j4
  mkdir $pkgdir/usr
  mkdir $pkgdir/usr/bin
  cp -r  "$srcdir/$name/$name" "$pkgdir/usr/bin/" 
}
