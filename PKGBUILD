# Maintainer: Rasmus Steinke <rasi at xssn dot at>
# Contributor: Christian Rebischke

pkgname=teiler
pkgver=v2.1.1
_pkgver=2.1.1
pkgrel=1
conflicts=('teiler-git')
provides=('teiler')
pkgdesc="a simple screenshot/screencast tool written in bash"
arch=('any')
url='https://github.com/carnager/teiler'
license=('GPL')
depends=('ffmpeg' 'maim' 'slop' 'xclip' 'dzen2' 'xininfo' 'rofi')
optdepends=('fb-client:         Upload to paste.xinu.at (or selfhosted filebin)'
            'openssh:           Upload to SSH server'
            'imgur:             Upload images to imgur.com'
            'copyq:             Image to Clipboard support'
            's3cmd:             Upload to s3 server')

options=(!strip)
install="teiler.install"
makedepends=()
source=($pkgname-$pkgver.tar.gz::$url/archive/$pkgver.tar.gz)

package () {
    cd ${srcdir}/${pkgname}-${_pkgver}
    make DESTDIR="$pkgdir/" \
        PREFIX='/usr' \
        install
}
md5sums=('321b73a4e8914c90e8f3a3e269d8dcf2')
