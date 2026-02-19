# note: I can't test arm64 support.

pkgname=biomejs-bin
pkgver=2.4.3
pkgrel=1
pkgdesc="A toolchain for the web: formatter, linter and more"
arch=('x86_64' 'aarch64')
url="https://github.com/biomejs/biome"
license=('MIT OR Apache-2.0')
depends=()
provides=('biome')
# too lazy to make a PKGBUILD to install from source or git lol
# conflicts=('biomejs')

source_x86_64=("biome::https://github.com/biomejs/biome/releases/download/@biomejs/biome@$pkgver/biome-linux-x64")
source_aarch64=("biome::https://github.com/biomejs/biome/releases/download/@biomejs/biome@$pkgver/biome-linux-arm64")
sha256sums_x86_64=('57484dcccb22f6a4379a021aef603283278cf4c3df5f84c0671ce3f98c9a90ae')
sha256sums_aarch64=('dff712430d076b65eafd54a64a11d992793b609d8101351a4a323f0aba3b028b')

# they publish BiomeJS to the NPM registry, but I wanted to make a PKGBUILD because why not (and of course, use it myself).
package() {
    local bin_name="biome"
    local bin_path="$srcdir/$bin_name"
    local dest_folder="$pkgdir/usr/bin"
    local bin_dest="$dest_folder/biome"
    mkdir -p $dest_folder
    # copy + make executable
    install -m 755 $bin_path "$bin_dest"
}