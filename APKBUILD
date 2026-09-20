# Reference: <https://postmarketos.org/devicepkg>
# Maintainer: YourLocalTechGuy <yourlocaldevguy@gmail.com>
pkgname=device-samsung-a22x
pkgver=1
pkgrel=1
pkgdesc="Samsung A22 5G"
url="https://postmarketos.org"
arch="aarch64"
license="MIT"

# THIS IS THE MISSING KEY:
_pmb_select_kernel="linux-samsung-a22x"

depends="
	linux-samsung-a22x
	postmarketos-base
	postmarketos-base-downstream
	android-tools
"
makedepends="devicepkg-dev"
source="
	deviceinfo
	modules-initfs
"
options="!archcheck !check"

build() {
	devicepkg_build $startdir $pkgname
}

package() {
	devicepkg_package $startdir $pkgname
}

sha512sums="
0f49a9de5f44b61dfe1839dfd747236a5f1646c7e99eefca69ee1b220f59e0ae019792305f09513aeb8bfbcd5db260152cd8102bb11d002a96eb4eb6e6bbb8fc  deviceinfo
e70bae17df23dcaaaea0e2d3616556f04baa23f8ee1357785c0f539bf97282d8ddff53953e155b72689bb73beb38c2da3d08de2a61e866684edfa10a6593885d  modules-initfs
"
