# Contributor: jorge_barroso <jorge.barroso.11@gmail.com>"
# Contributor: mar77i <mysatyre at gmail dot com>"

_debname=iceweasel
_debver=14.0.1
_debrel=2
_debrepo=http://ftp.debian.org/debian/pool/main/

pkgname=iceweasel-il18n-en-za
pkgver=$_debver.$_debrel
pkgrel=3

pkgdesc="Language packs for Debian Iceweasel."
arch=('any')
url="http://www.geticeweasel.org/"
license=('MPL')
depends=("iceweasel>=$_debver")

source=("$_debrepo/${_debname:0:1}/$_debname/$_debname-l10n-en-za_${_debver}-${_debrel}_all.deb")
md5sums=(5a7189208bb083164a37294b0906df6b)

build() {
	cd "$srcdir"
	bsdtar xf "${source##*/}"
	bsdtar xf data.tar.gz
}

package() {
	install -Dm644 "$srcdir/usr/lib/iceweasel/extensions/langpack-en-za@iceweasel.mozilla.org.xpi"                    "$pkgdir/usr/lib/iceweasel/extensions/langpack-en-za@iceweasel.mozilla.org.xpi"
}

