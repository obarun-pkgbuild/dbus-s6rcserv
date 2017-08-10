# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=dbus-s6rcserv
pkgver=0.1
pkgrel=3
pkgdesc="dbus service for s6"
arch=(x86_64)
license=('beerware')
depends=('dbus' 's6' 's6-rc' 's6-boot')
conflicts=()
install=dbus-s6rcserv.install
source=('dbus.prepare.dependencies.s6'
		'dbus.prepare.type.s6'
		'dbus.prepare.up.s6'
		
		'dbus.daemon.dependencies.s6'
		'dbus.daemon.finish.s6'
		'dbus.daemon.pipeline-name.s6'
		'dbus.daemon.producer-for.s6'
		'dbus.daemon.run.s6'	
		'dbus.daemon.type.s6'	
		
		'dbus.log.consumer-for.s6'
		'dbus.log.dependencies.s6'
		'dbus.log.run.s6'
		'dbus.log.type.s6'
		
		'bundle.dbus.contents.s6'
		'bundle.dbus.type.s6'
		'LICENSE')
md5sums=('68b329da9893e34099c7d8ad5cb9c940'
         '85bceea1fb94d4166f24496dc40a35e6'
         'ff82cde1c60640c50067af955c4c00a0'
         '43c1ce8f19d9191fd6a3a75df32e7c2f'
         '59a28e06e3d99a59ef4f6b9ce7418be0'
         'c7ddb8398cd5c587d087e5bb2615d773'
         'c310f970ba1b740e56d61c6bca3fd810'
         'ffa2d99aad0507f7b4f27442680e5969'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         '80f7ac8a34abebb83908831b1426189e'
         '68b329da9893e34099c7d8ad5cb9c940'
         '0796d3c4d0b6b07a31783b339c7aff27'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'daa3787858e0189413580f4fdf9766de'
         '71abe97e2554d37f1d12c5bf4945297f'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# bundle , trouble here user-dbus need a maj at dbus e.g user-Base
	install -Dm 0644 "$srcdir/bundle.dbus.contents.s6" "$pkgdir/etc/s6-serv/available/rc/bundle-Dbus/contents"
	install -Dm 0644 "$srcdir/bundle.dbus.type.s6" "$pkgdir/etc/s6-serv/available/rc/bundle-Dbus/type"
	
	#prepare
	install -Dm 0644 "$srcdir/dbus.prepare.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/dbus-prepare/dependencies"
	install -Dm 0644 "$srcdir/dbus.prepare.type.s6" "$pkgdir/etc/s6-serv/available/rc/dbus-prepare/type"
	install -Dm 0644 "$srcdir/dbus.prepare.up.s6" "$pkgdir/etc/s6-serv/available/rc/dbus-prepare/up"
	
	# daemon
	install -Dm 0644 "$srcdir/dbus.daemon.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/dbus-daemon/dependencies"
	install -Dm 0644 "$srcdir/dbus.daemon.finish.s6" "$pkgdir/etc/s6-serv/available/rc/dbus-daemon/finish"
	install -Dm 0644 "$srcdir/dbus.daemon.pipeline-name.s6" "$pkgdir/etc/s6-serv/available/rc/dbus-daemon/pipeline-name"
	install -Dm 0644 "$srcdir/dbus.daemon.producer-for.s6" "$pkgdir/etc/s6-serv/available/rc/dbus-daemon/producer-for"
	install -Dm 0644 "$srcdir/dbus.daemon.run.s6" "$pkgdir/etc/s6-serv/available/rc/dbus-daemon/run"
	install -Dm 0644 "$srcdir/dbus.daemon.type.s6" "$pkgdir/etc/s6-serv/available/rc/dbus-daemon/type"
	
	# log
	install -Dm 0644 "$srcdir/dbus.log.consumer-for.s6" "$pkgdir/etc/s6-serv/available/rc/dbus-log/consumer-for"
	install -Dm 0644 "$srcdir/dbus.log.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/dbus-log/dependencies"
	install -Dm 0644 "$srcdir/dbus.log.run.s6" "$pkgdir/etc/s6-serv/available/rc/dbus-log/run"
	install -Dm 0644 "$srcdir/dbus.log.type.s6" "$pkgdir/etc/s6-serv/available/rc/dbus-log/type"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/dbus-s6rcserv/LICENSE"
}
