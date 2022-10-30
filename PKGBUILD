# Maintainer: Novus <novusoh01@outlook.com>
pkgname=novos-classic-wallpapers
pkgver=20221014
pkgrel=1
pkgdesc="All desktop wallpapers for projects before NovOS linux are provided here."
arch=('any')
url="https://github.com/NovOS-Linux/novos-classic-wallpapers"
license=('MIT')
depends=('desktop-file-utils' 'hicolor-icon-theme')
makedepends=('git')
source=("git+$url")
md5sums=('SKIP')

pkgver() {
	cd "$pkgname"
	echo $(TZ=UTC git log -1 --pretty='%cd' --date=short-local | tr -d '-')
}

package() {
	cd "$pkgname"
	install -Dm644 Wallpapers/* -t "$pkgdir/usr/share/backgrounds/$pkgname/"
	install -Dm644 "LICENSE.md" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
