# Maintainer: agnotek <agnostic [dot] sn [at] gmail [dot] com>

pkgname=ytplmp4
pkgver=7.2
pkgrel=1
pkgdesc="YTPLMP4 - YouTube Playlist to MP3. Download single songs or playlists from Youtube and Soundcloud."
arch=('any')
url="http://youtube.com/"
license=('GPL3')
makedepends=('')
depends=('id3v2' 'python2-eyed3' 'youtube-dl' 'yad' 'curl' 'feh' 'recode' 'smplayer' 'ffmpeg' 'perl-image-exiftool' 'lame')
options=('!strip')
install="ytplmp4.install"
md5sums=('735a46179d409e3f34c39a5c609fb680'
         '9347b695d57d40c8756fcb593f28158c'
         'ceae8591b64a369118d4928042cfb403')

source=("https://dl.dropboxusercontent.com/u/9839330/YTPLMP3/YTPLMP4-${pkgver}.tar.gz"
        "ytplmp4.install"
        "ytplmp4.desktop")

package() {
  cd "${srcdir}"

  install -dm755 "${pkgdir}/usr/share/${pkgname}"
  install -dm755 "${pkgdir}/usr/bin"

  # Program
  echo "${pkgdir}/usr/share/${pkgname}/"
  install -Dm755 ${srcdir}/YTPLMP4 "${pkgdir}/usr/share/${pkgname}/"

  # Link to program
  mkdir -p "${pkgdir}/usr/bin"
  ln -s "/usr/share/${pkgname}/YTPLMP4" "${pkgdir}/usr/bin/YTPLMP4"

  # Desktop file
  install -Dm644 "${srcdir}/ytplmp4.desktop" "${pkgdir}/usr/share/applications/ytplmp4.desktop"

}

