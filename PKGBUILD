pkgname=speedtest-cli
pkgver=2.0.2
pkgrel=1
pkgdesc='Command line interface for testing internet bandwidth using speedtest.net'
arch=('x86_64')
url='https://github.com/sivel/speedtest-cli'
license=('Apache')
depends=('python3-setuptools')
source=("https://github.com/sivel/speedtest-cli/archive/v${pkgver}.tar.gz")
sha512sums=('12fa9a5dd8bcb7a7ee68ecc9075dc5c18f089cecf003e7e643dbb6b1c3663f17c2aba48d1e84aa27bff6b66e207d39ecaf874aebad1d71cac772c58b62191723')

build() {
  cd ${pkgname}-${pkgver}
  python setup.py build
}

package(){
  cd ${pkgname}-${pkgver}
  python setup.py install -O1 --root="${pkgdir}" --prefix=/usr --skip-build
  install -Dm 644 LICENSE -t "${pkgdir}/usr/share/licenses/${pkgname}"
  install -Dm 644 README.rst -t "${pkgdir}/usr/share/doc/${pkgname}"
  install -Dm 644 ${pkgname}.1 -t "${pkgdir}/usr/share/man/man1"
}
