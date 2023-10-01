# Maintainer: 3rice <github.com/X3ric>
pkgname=walengine
pkgver=3__2023.10.01
pkgrel=1
pkgdesc='A simple background web browser based on WebKit/GTK+.'
arch=('x86_64')
url="https://github.com/X3ric/${pkgname}"
license=('MIT')
depends=('webkit2gtk' 'gcr' 'xorg-xprop')
makedepends=('git')  # Add any build dependencies here
source=("git+https://github.com/X3ric/walengine.git")
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/${pkgname}"
  _tag=$(git describe --tags | sed 's:^v::')
  _commits=$(git rev-list --count HEAD)
  _date=$(git log -1 --date=short --pretty=format:%cd)
  printf "%s_%s_%s\n" "${_commits}" "${_tag}" "${_date}" | sed 's/-/./g'
}

build() {
  cd "$srcdir/${pkgname}"
  make
}

package() {
  cd "$srcdir/${pkgname}"
  make PREFIX=/usr DESTDIR="${pkgdir}" install

  # Install the license file with a more specific name
  install -Dm0644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
