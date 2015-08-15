# Maintainer: Tomasz Wisniewski <tomasz.wisni3wski@gmail.com>
pkgname=bashnapi
pkgver=1.3.4
pkgrel=1
pkgdesc="napiprojekt.pl bash client and universal subtitle converter"
arch=('any')
url="http://sourceforge.net/projects/bashnapi"
license=('GPL')
groups=()
depends=('bash' 'coreutils' 'sed' 'gawk' 'grep' 'findutils' 'wget')
makedepends=()
optdepends=()
provides=()
conflicts=('subotage')
replaces=()
backup=()
options=()
install=
changelog=
source=("http://sourceforge.net/projects/${pkgname}/files/${pkgname}_v${pkgver}.tar.gz/download")
noextract=()
md5sums=('ea89bfa2203ceb12b4a56f37eb07f72a')

build() {
	echo "nothing to do"
}

package() {
	mkdir -p ${pkgdir}/usr/bin
	mkdir -p ${pkgdir}/usr/share/napi
	cd ${srcdir}/napi-${pkgver}

	sed -i "s|NAPI_COMMON_PATH=|NAPI_COMMON_PATH=/usr/share/napi|" napi.sh
	sed -i "s|NAPI_COMMON_PATH=|NAPI_COMMON_PATH=/usr/share/napi|" subotage.sh

	cp -v subotage.sh napi.sh ${pkgdir}/usr/bin
	cp -v napi_common.sh ${pkgdir}/usr/share/napi
}
