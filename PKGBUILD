# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=dbus-s6rcserv
pkgver=0.1
pkgrel=4
pkgdesc="dbus service for"
arch=(x86_64)
license=('beerware')
depends=('dbus' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('dbus.prepare.dependencies'
		'dbus.prepare.type'
		'dbus.prepare.up'
		
		'dbus.longrun.dependencies'
		'dbus.longrun.finish'
		'dbus.longrun.pipeline-name'
		'dbus.longrun.producer-for'
		'dbus.longrun.run'	
		'dbus.longrun.type'	
		
		'dbus.log.consumer-for'
		'dbus.log.dependencies'
		'dbus.log.run'
		'dbus.log.type'
		
		'bundle.dbus.contents'
		'bundle.dbus.type'
		'dbus.logd'
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
         '0ef8d10b039296360d6cbba81b0c8d55'
         '68b329da9893e34099c7d8ad5cb9c940'
         '0796d3c4d0b6b07a31783b339c7aff27'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'fd43c23786d66bd2f5b53d2f0b85d3a3'
         '71abe97e2554d37f1d12c5bf4945297f'
         '080934ecba23de8c4a288e7a5b4a2a73'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# bundle , trouble here user-dbus need a maj at dbus e.g user-Base
	install -Dm 0644 "$srcdir/bundle.dbus.contents" "$pkgdir/etc/s6-serv/available/rc/bundle-Dbus/contents"
	install -Dm 0644 "$srcdir/bundle.dbus.type" "$pkgdir/etc/s6-serv/available/rc/bundle-Dbus/type"
	
	#prepare
	install -Dm 0644 "$srcdir/dbus.prepare.dependencies" "$pkgdir/etc/s6-serv/available/rc/dbus-prepare/dependencies"
	install -Dm 0644 "$srcdir/dbus.prepare.type" "$pkgdir/etc/s6-serv/available/rc/dbus-prepare/type"
	install -Dm 0644 "$srcdir/dbus.prepare.up" "$pkgdir/etc/s6-serv/available/rc/dbus-prepare/up"
	
	# longrun
	install -Dm 0644 "$srcdir/dbus.longrun.dependencies" "$pkgdir/etc/s6-serv/available/rc/dbus-longrun/dependencies"
	install -Dm 0644 "$srcdir/dbus.longrun.finish" "$pkgdir/etc/s6-serv/available/rc/dbus-longrun/finish"
	install -Dm 0644 "$srcdir/dbus.longrun.pipeline-name" "$pkgdir/etc/s6-serv/available/rc/dbus-longrun/pipeline-name"
	install -Dm 0644 "$srcdir/dbus.longrun.producer-for" "$pkgdir/etc/s6-serv/available/rc/dbus-longrun/producer-for"
	install -Dm 0644 "$srcdir/dbus.longrun.run" "$pkgdir/etc/s6-serv/available/rc/dbus-longrun/run"
	install -Dm 0644 "$srcdir/dbus.longrun.type" "$pkgdir/etc/s6-serv/available/rc/dbus-longrun/type"
	
	# log
	install -Dm 0644 "$srcdir/dbus.log.consumer-for" "$pkgdir/etc/s6-serv/available/rc/dbus-log/consumer-for"
	install -Dm 0644 "$srcdir/dbus.log.dependencies" "$pkgdir/etc/s6-serv/available/rc/dbus-log/dependencies"
	install -Dm 0644 "$srcdir/dbus.log.run" "$pkgdir/etc/s6-serv/available/rc/dbus-log/run"
	install -Dm 0644 "$srcdir/dbus.log.type" "$pkgdir/etc/s6-serv/available/rc/dbus-log/type"
	
	# hook
	install -Dm 0644 "$srcdir/dbus.logd" "$pkgdir/etc/s6-serv/log.d/dbus-rc"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/dbus-s6rcserv/LICENSE"
}
