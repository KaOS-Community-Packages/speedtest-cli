pkgname=speedtest-cli
pkgver=0.3.4
pkgrel=1
pkgdesc='Command line interface for testing internet bandwidth using speedtest.net'
arch=('x86_64')
url='https://github.com/sivel/speedtest-cli'
license=('Apache')
depends=('python3')
source=("https://github.com/sivel/speedtest-cli/archive/v${pkgver}.tar.gz")
sha512sums=('fb22ba9e17a30c172b8f751020d7117caf8b573dee112506917f24c5173e2901e0f0198b4946798daf3a27839519025f4a7f8f8942034bc19356b32d6a0f6851')

package(){
    cd "$srcdir/$pkgname-$pkgver"

    install -D -m755 speedtest_cli.py "${pkgdir}/usr/bin/speedtest-cli"
    install -D -m644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
