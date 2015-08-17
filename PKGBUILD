# Maintainer: Flaviu Tamas <tamas.flaviu@gmail.com>
pkgname=pdfbooklet
_realpkgname=pdfBooklet
pkgver=2.2.2
pkgrel=4
pkgdesc="A Python script whose first purpose was to create booklet(s) from existing pdf files. It has been extended to many other functions in pdf pages manipulation. "
url="http://pdfbooklet.sourceforge.net/"
arch=('any')
license=('GPL3')
depends=('python2' 'python2-poppler')
source=("http://downloads.sourceforge.net/project/pdfbooklet/pdfBooklet-pdfShuffler%202.2.2/pdfBooklet-2.2.2.tar.gz"
        "pdfbooklet.patch")
md5sums=('f71dfad26585c2fe2dba1e52aaab4bf5'
         'bf7b6d6b5ad44f1b33e1874ab4a89fbf')

build(){
  cd "$srcdir/$_realpkgname-$pkgver"
  patch -p1 -i $srcdir/$pkgname.patch 
}

package() {
  cd "$srcdir/$_realpkgname-$pkgver"
  python2 setup.py install --root="$pkgdir/" --optimize=1
}

# vim:set ts=2 sw=2 et:
