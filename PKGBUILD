# Maintainer:   Lucky <archlinux@builds.lucky.li>
# Contributor:  Farhad Shahbazi <farhad@enthusiasm.cc>
#
# Merge stuff from: puddletag-hg
# (https://aur.archlinux.org/packages.php?ID=56050)

pkgname=puddletag
pkgver=1.0.1
pkgrel=3
pkgdesc="An audio tag editor for GNU/Linux (like Mp3tag)"
url="http://puddletag.sourceforge.net"
license=("GPL")
arch=("any")
depends=("python2>=2.5" "python2-configobj>=4.5.0" "python2-musicbrainz2>=0.6.0" "python2-pyqt4>=4.5" "python2-pyparsing>=1.5.1" "mutagen>=1.20")
optdepends=("python2-imaging: edit/view FLAC cover art"
            "quodlibet: edit a QuodLibet library")
source=("http://downloads.sourceforge.net/project/${pkgname}/${pkgname}-${pkgver}.tar.gz")
md5sums=("bf04676b94b625b5df854e45f6755d7e")
sha1sums=("09cf2db36ec13ab2a5ac53d871e2b04b0f5afa48")

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"

  python2 setup.py config
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"

  python2 setup.py install --prefix="${pkgdir}/usr" --optimize=1
}
