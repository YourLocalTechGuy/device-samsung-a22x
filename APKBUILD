# Reference: <https://postmarketos.org/devicepkg>
# Maintainer: YourLocalTechGuy <yourlocaldevguy@gmail.com>
pkgname=device-samsung-a22x
pkgver=1
pkgrel=2
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
    mt6359-sia8109.tar.gz
    conn.conf
"

#options="!archcheck !check"

build() {
    devicepkg_build $startdir $pkgname
}

package() {
    devicepkg_package $startdir $pkgname
    install -Dm644 "$srcdir/99-blobs.files" "$pkgdir/etc/mkinitfs/files/99-blobs.files"           

    # Install the ALSA UCM directory recursively to the correct target path
    mkdir -p "$pkgdir/usr/share/alsa/ucm2/MediaTek/mt6833/"
    tar -xzf "$srcdir/mt6359-sia8109.tar.gz" -C "$pkgdir/usr/share/alsa/ucm2/MediaTek/mt6833"
    install -Dm644 "$srcdir/conn.conf" "$pkgdir/etc/modules-load.d/conn.conf"
}

sha512sums="
7c33f0eafd0b6a8ea16f15caa4c39fb4b68794ecb7398d41097390d457d25d1d5aebf64305ecd49e03b5e77b99e08ebc82ace36f307f024eb32f259b7c8ed17e  deviceinfo
e70bae17df23dcaaaea0e2d3616556f04baa23f8ee1357785c0f539bf97282d8ddff53953e155b72689bb73beb38c2da3d08de2a61e866684edfa10a6593885d  modules-initfs
9b696a81d0a99c70c8c75129a45273879bf73270027bf8e1e6ef3c05181001621994c3eecf784173f36068defeea9cefe072842dfa316422a34a8056c8c60f7d  99-blobs.files
24c052cea8308caf6a4398991892838635e5f6651d0ecd264810353d4b36ed9b334a1e5749f1c1e31fab8501d66186e1d8fb84ff5ecb09fe08fd986ee9719d04  mt6359-sia8109.tar.gz
7b24fc2b0fea6a414cd0269e21c81c89b4cb3905bc21fb8604b5bf78d100d5498b66c63afeecc14b3f81038cf0cf14097d4a00942ac74cdb771020780bc6da64  conn.conf
"
