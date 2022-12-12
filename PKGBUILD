pkgname="magic-commit"
pkgver=0.1.4
pkgrel=1
pkgdesc="A CLI tool that generates commit messages from your staged changes, using OpenAI Codex."
arch=("x86_64" "arm")
license=("mit")
url='https://github.com/rookasrudzianskas/commit-open-ai'
makedepends=("git")
source=("git+https://github.com/rookasrudzianskas/commit-open-ai")
sha512sums=("SKIP")

pkgver() {
  cd "$pkgname"
  git describe --tags | sed 's/^v//;s/\([^-]*-g\)/r\1/;s/-/./g'
}

package() {
    cd auto-commit
    bash "./install.sh"
}
