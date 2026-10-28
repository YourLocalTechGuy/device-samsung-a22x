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
    firmware-samsung-a22x
    linux-samsung-a22x
    postmarketos-base
    android-tools
"
makedepends="devicepkg-dev"
source="
    deviceinfo
    modules-initfs
    99-fuckingwork.files
"

#options="!archcheck !check"

build() {
    devicepkg_build $startdir $pkgname
}

package() {
    devicepkg_package $startdir $pkgname
}

sha512sums="
54453cb2a6d125b878addcf34f8c53be7b68e819231fa8a642b90cea9c8569ca98d596c10715db3c78476fefcd8097501662bcc7632649bd79b3e8ff1fdee5e0  deviceinfo
e70bae17df23dcaaaea0e2d3616556f04baa23f8ee1357785c0f539bf97282d8ddff53953e155b72689bb73beb38c2da3d08de2a61e866684edfa10a6593885d  modules-initfs
9b696a81d0a99c70c8c75129a45273879bf73270027bf8e1e6ef3c05181001621994c3eecf784173f36068defeea9cefe072842dfa316422a34a8056c8c60f7d  99-fuckingwork.files
"
