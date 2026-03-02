# note: I can't test arm64 support.

pkgname=biomejs-bin
pkgver=2.4.5
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
sha256sums_x86_64=('a31815f19b0b90fa043eb23fbf769ed931fbcde6d98bb89894ea8be1387d8394')
sha256sums_aarch64=('98a109d54bfea7df1e82b73aa7d37fc2caa880d12105eb2495efe0d653955518')

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