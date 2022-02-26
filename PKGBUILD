# Maintainer: Drommer <drommer@github.com>

pkgname=sweet-cursor-theme-git
_pkgname=sweet
pkgver=r218.741c4f3
pkgrel=1
pkgdesc="Colorful Sweet GTK and KDE theme"
arch=('any')
url="https://github.com/EliverLara/$_pkgname"
license=('GPL3')
source=("git+$url.git#branch=nova")
sha256sums=('SKIP')
makedepends=('git')

pkgver() {
	cd "$srcdir/$_pkgname"
	printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package_sweet-cursor-theme-git() {
	provides=('sweet-cursor-theme' 'xcursor-sweet')
	conflicts=('xcursor-sweet')
	pkgdesc="Sweet cursor theme"
	cd $_pkgname/kde
	install -d $pkgdir/usr/share/icons
	mv cursors/Sweet-cursors "$pkgdir/usr/share/icons"
}
