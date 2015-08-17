# Maintainer: edoardo <edoardo.elidoro@gmail.com>
# Contributor: syne <madlikene@aim.com>

pkgname=nspluginwrapper-flash-prerelease
pkgver=11.2.202.197
pkgrel=1
pkgdesc="32-bit flash 11.2beta3 prerelease for arch64"
url='http://labs.adobe.com/technologies/flashplatformruntimes/flashplayer11-2/'
license=('custom')
conflicts=('flashplugin')
depends=('nspluginwrapper' 'lib32-nss' 'lib32-curl' 'lib32-gtk2' 'lib32-alsa-lib' 'lib32-libxt' 'mozilla-common')
optdepends=('lib32-libflashsupport-oss: for OSS users who have no sound after install'
'lib32-alsa-plugins: for PulseAudio support')
arch=('x86_64')
install=('plugin.install')
source=('http://download.macromedia.com/pub/labs/flashplatformruntimes/flashplayer11-2/flashplayer11-2_p5_install_lin_32_013112.tar.gz' 'adobe_eula.txt')
md5sums=('1e5fd6e6c688a39ddfadae96fe74f69d')

build () {
cd $startdir/pkg
install -D -m755 $startdir/src/libflashplayer.so $startdir/pkg/usr/lib/mozilla/plugins/libflashplayer.so
install -D -m644 $startdir/src/adobe_eula.txt $startdir/pkg/usr/share/licenses/$pkgname/LICENSE || return 1
}