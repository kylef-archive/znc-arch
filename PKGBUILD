pkgname=znc-system-wide
pkgver=1.0
pkgrel=1
pkgdesc=''
arch=('any')
license=('GPL2')
depends=('znc')
install=znc.install

source=(znc.rcd znc.conf)
md5sums=('7d8ea0b63e3d898bad6c1370fc52530c'
         '31a7b5a79c364b9159b5c968045c5cdc')

package() {
  install -D -m755 znc.rcd "$pkgdir"/etc/rc.d/znc
  install -D -m644 znc.conf "$pkgdir"/etc/conf.d/znc

  install -o143 -g143 -dm750 "$pkgdir"/var/lib/znc
}
