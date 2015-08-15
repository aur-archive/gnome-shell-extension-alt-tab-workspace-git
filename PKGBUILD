# Maintainer: jtts
# Contributor: Christian METZLER <neroth@xeked.com> (gnome-shell-extension-weather-git was used as a template)

pkgname=gnome-shell-extension-alt-tab-workspace-git
pkgver=20140503
pkgrel=1
pkgdesc="A GNOME Shell extension, which replaces Alt-Tab to cycle through apps on current workspace only."
arch=('any')
url="https://github.com/kwalo/gnome-shell-alt-tab-workspace"
license=('GPL3')
depends=('gnome-shell')
makedepends=('git')
#replaces=('')
install='gnome-shell-extension.install'
source=("$pkgname"::"git+https://github.com/kwalo/gnome-shell-alt-tab-workspace"
	"gnome-shell-3.12.diff")
sha256sums=('SKIP'
            'd3aa979989659a8c30b7d61c7ad07660adf58d1547319c3ad689c4c947b0a65c')

prepare() {
  cd "$srcdir"
  patch -p0 < gnome-shell-3.12.diff
}

package() {
  cd "$srcdir/$pkgname"
  install -Dm644 README $pkgdir/usr/share/gnome-shell/extensions/alt-tab-workspace@kwalo.net/README
  install -Dm644 alt-tab-workspace@kwalo.net/extension.js $pkgdir/usr/share/gnome-shell/extensions/alt-tab-workspace@kwalo.net/extension.js
  install -Dm644 alt-tab-workspace@kwalo.net/metadata.json $pkgdir/usr/share/gnome-shell/extensions/alt-tab-workspace@kwalo.net/metadata.json
  install -Dm644 alt-tab-workspace@kwalo.net/stylesheet.css $pkgdir/usr/share/gnome-shell/extensions/alt-tab-workspace@kwalo.net/stylesheet.css
}
