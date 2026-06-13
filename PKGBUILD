# Maintainer: m4teo.dev <m4teo.dev@gmail.com>

pkgname=helix-calamares-config
pkgver=2.1
pkgrel=4
pkgdesc="Calamares config for Helix Linux"
arch=('any')
url="https://github.com/archlatam/helix-calamares-config"
license=('GPL3')
makedepends=('git')
depends=()
provides=("${pkgname}")
options=(!strip !emptydirs)
source=("${pkgname}::git+https://github.com/archlatam/helix-calamares-config.git#branch=main")
sha256sums=('SKIP')

package() {
  cd "${srcdir}/${pkgname}/etc/calamares"

  # settings.conf
  install -Dm644 settings.conf "${pkgdir}/etc/calamares/settings.conf"

  # branding
  install -dm755 "${pkgdir}/etc/calamares/branding/default"
  cp -r branding/default/* "${pkgdir}/etc/calamares/branding/default/"

  # módulos
  install -dm755 "${pkgdir}/etc/calamares/modules"
  cp -r modules/* "${pkgdir}/etc/calamares/modules/"

  # scripts
  install -dm755 "${pkgdir}/etc/calamares/scripts"
  cp -r scripts/* "${pkgdir}/etc/calamares/scripts/"
}
