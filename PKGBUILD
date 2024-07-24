# Maintainer: Mysti

pkgname=proton-pass-bin
pkgver=1.20.1
pkgrel=1
pkgdesc="Open-source password manager for effortless protection. Securely store, share and auto-login your accounts with Proton Pass, using end-to-end encryption trusted by millions."
arch=("x86_64")
url="https://proton.me/pass"
groups=("ProtonPass")
source=("https://proton.me/download/PassDesktop/linux/x64/ProtonPass_${pkgver}.deb")
sha256sums=('1b5e3f8157afbdc715f082cfafbd3520ff24ad1dbf98e9d19f489c08fd478b8b')
conflicts=('proton-pass' 'protonpass')
replaces=('proton-pass' 'protonpass')

package() {
	tar -xvf data.tar.xz -C "$pkgdir/"

	install -d "$pkgdir/opt/"
	mv "$pkgdir/usr/lib/proton-pass" "$pkgdir/opt/"

	ln -sf "/opt/proton-pass/Proton Pass" "$pkgdir/usr/bin/proton-pass"

	rm -rf "$pkgdir"/usr/share/{doc,lintian}
}
