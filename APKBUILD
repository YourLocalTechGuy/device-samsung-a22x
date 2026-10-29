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
    99-blobs.files
"

#options="!archcheck !check"

build() {
    devicepkg_build $startdir $pkgname
}

package() {
    devicepkg_package $startdir $pkgname
    install -Dm644 "$srcdir/99-blobs.files" "$pkgdir/etc/mkinitfs/files/99-blobs.files"           
}

sha512sums="
9f3f5d75d20ed54cb7f51078e2865cc920b4a617cc1fc86f8483a3345536943cbb939e08101ee3a5012d36df2c9d76b337fd40e0401cf50fba50469132d5b4ab  deviceinfo
e70bae17df23dcaaaea0e2d3616556f04baa23f8ee1357785c0f539bf97282d8ddff53953e155b72689bb73beb38c2da3d08de2a61e866684edfa10a6593885d  modules-initfs
9b696a81d0a99c70c8c75129a45273879bf73270027bf8e1e6ef3c05181001621994c3eecf784173f36068defeea9cefe072842dfa316422a34a8056c8c60f7d  99-blobs.files
"
