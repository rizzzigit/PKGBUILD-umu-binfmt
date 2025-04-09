# Maintainer: Rizzzi Git <rizzzigit@gmail.com>

pkgname="umu-binfmt"
pkgdesc="binfmt registration & desktop entry for umu-launcher"
pkgrel=1
epoch=0
pkgver=1.0

arch=("x86_64")
license=("GPL-3.0")
depends=('umu-launcher')
conflicts=('wine' 'wine-staging')

src=(
  "umu-launch.desktop"
  "umu-launch.sh"
  "umu-launch.conf"
)

package() {
  mkdir -pm 755 "$pkgdir/usr/share/applications"
  mkdir -pm 755 "$pkgdir/opt/umu-binfmt"
  mkdir -pm 755 "$pkgdir/usr/lib/binfmt.d"

  install -Dm644 "$startdir/umu-launch.desktop" "$pkgdir/usr/share/applications/"
  install -Dm755 "$startdir/umu-launch.sh" "$pkgdir/opt/umu-binfmt/"
  install -Dm644 "$startdir/umu-launch.conf" "$pkgdir/usr/lib/binfmt.d/umu-launch.conf"
}
