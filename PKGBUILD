# Maintainer: jsteel <mail at jsteel dot org>
# Contributor: Nathan Owe <ndowens.aur at gmail dot com>
# Contributor: Giovanni Scafora <giovanni@archlinux.org>
# Maintainer: Marius Nestor <marius at softpedia dot com>

pkgname=flvtomp3
pkgver=1.2.1
pkgrel=3
pkgdesc="Permits you to extract the sound track of a .flv file without loss of quality"
arch=('i686' 'x86_64')
url="http://sourceforge.net/projects/flvtomp3"
license=('GPLv2')
depends=('qt4')
source=(http://downloads.sourceforge.net/$pkgname/FlvToMp3_${pkgver}_source.tar.gz
        $pkgname.desktop)
md5sums=('3f38088601ca4becee6fc9b2c5ede222'
         'f2e0fbb1d6a92984a8bc8900cdd6f576')

build() {
  cd "$srcdir"/FlvToMp3

  qmake-qt4
  make
}

package() {
  cd "$srcdir"/FlvToMp3

  install -Dm755 FlvToMp3 "$pkgdir"/usr/bin/FlvToMp3
  install -Dm644 icone.ico "$pkgdir"/usr/share/pixmaps/flvtomp3.ico
  install -Dm644 "$srcdir"/$pkgname.desktop "$pkgdir"/usr/share/applications/$pkgname.desktop
}
