# Maintainer: Ulrich Ölmann <ulrich.oelmann@web.de>
# Maintainer: akliuxingyuan
pkgname='mkinitcpio-kpartx'
pkgver=1.0.0
pkgrel=1
pkgdesc='mkinitcpio hook allowing for a GPT partitioned LUKS device not needing LVM'
url='https://github.com/akliuxingyuan/mkinitcpio-kpartx'
arch=('any')
license=('custom:0BSD')
depends=('mkinitcpio' 'multipath-tools')
install="$pkgname.install"
source=('kpartx_hook' 'kpartx_install' '0BSD')
sha256sums=('2c64349c23356fef579dada3943a60f23b43e00fcb450eb467dd6d2e10a21683'
            '534b699571e345a508b31570c95ebae164351ad0052aca001f067b0cbde6b9f4'
            '8bfb255ba92f14f6b0c7e3a47fc6276293a56e26838358ca63e892e008eeb8d2')

package() {
    install --owner=root --group=root --mode=0644 -D ${srcdir}/kpartx_hook    ${pkgdir}/usr/lib/initcpio/hooks/kpartx
    install --owner=root --group=root --mode=0644 -D ${srcdir}/kpartx_install ${pkgdir}/usr/lib/initcpio/install/kpartx
    install --owner=root --group=root --mode=0644 -D ${srcdir}/0BSD           ${pkgdir}/usr/share/licenses/${pkgname}/0BSD
}
