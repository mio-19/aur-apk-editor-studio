# Maintainer: Clansty <i@gao4.pw>

pkgname=yesplaymusic-electron
pkgver=0.3.7
pkgrel=1
pkgdesc="A third party music application for Netease Music. Using the system electron"
arch=("any")
url="https://github.com/qier222/YesPlayMusic"
license=("MIT")
depends=(
    "gtk3"
    "nss"
    "electron"
)
optdepends=(
    'c-ares'
    'ffmpeg'
    'http-parser'
    'libevent'
    'libvpx'
    'libxslt'
    'minizip'
    're2'
    'snappy'
    'libnotify'
    'libappindicator-gtk3'
)
source=(
    "YesPlayMusic-${pkgver}.pacman::https://github.com/qier222/YesPlayMusic/releases/download/v${pkgver}/YesPlayMusic-${pkgver}.pacman"
    yesplaymusic.desktop
)
md5sums=('acf05f038cc7a1ad42db439c098e6f41'
         '107bf43817d58d29486823343ea36050')

package() {
    cp -r "usr" "${pkgdir}"
    rm "${pkgdir}/usr/share/applications/yesplaymusic.desktop"
    install -d "${pkgdir}/usr/share"
    install -Dm644 -t "${pkgdir}/usr/share/applications" "yesplaymusic.desktop"
    install -Dm644 "opt/YesPlayMusic/resources/app.asar" "${pkgdir}/usr/share/yesplaymusic.asar"
}
