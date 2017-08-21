# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=dhcpcd-s6serv
pkgver=0.1
pkgrel=4
pkgdesc="dhcpcd service for s6"
arch=(x86_64)
license=('beerware')
depends=('dhcpcd' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('dhcpcd.daemon.finish.s6'
		'dhcpcd.daemon.run.s6'
		'dhcpcd.log.run.s6'
		'dhcpcd.logd'
		'LICENSE')
md5sums=('85a07b0c36eb556d5ca634daaf7540c2'
         '97eb90878e192d23a786e92eab440705'
         '65fae0a904e3459401f35f61317d57a8'
         '7286587f41043f53e437b27ca4dbb55e'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/dhcpcd.daemon.finish.s6" "$pkgdir/etc/s6-serv/available/classic/dhcpcd/finish"
	install -Dm 0755 "$srcdir/dhcpcd.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/dhcpcd/run"
	
	# log
	install -Dm 0755 "$srcdir/dhcpcd.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/dhcpcd/log/run"
	install -Dm 0644 "$srcdir/dhcpcd.logd" "$pkgdir/etc/s6-serv/log.d/serv/dhcpcd"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/dhcpcd-s6serv/LICENSE"
}
