# Maintainer: Cecile Tonglet <cecile.tonglet@gmail.com>

pkgname="retroarch-rbp-bin"
pkgver="1.3.2"
pkgrel=1
pkgdesc="Simple frontend for the Libretro API"
arch=('arm' 'armv6h' 'armv7h')
url="http://www.libretro.com"
license=('GPL')
provides=('retroarch')
conflicts=('retroarch' 'retroarch-git')
depends=('python' 'libusb' 'libxkbcommon' 'alsa-lib' 'raspberrypi-firmware-tools' 'freetype2' 'sdl2')
source=(
  "http://downloads.petrockblock.com/retropiebinaries/jessie/rpi2/emulators/retroarch.tar.gz"
)

md5sums=(
  'b86dfce155c294fc10db728fb884c839'
)

package() {
    mkdir $pkgdir/usr || return 1
    cp -a $srcdir/retroarch/bin $pkgdir/usr/ || return 1
    cp -a $srcdir/retroarch/share $pkgdir/usr/share || return 1
    mkdir $pkgdir/etc || return 1
    cp $srcdir/retroarch/retroarch.cfg $pkgdir/etc/retroarch.cfg || return 1
}
