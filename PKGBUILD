# Author : MrMen <tetcheve at gmail dot com> 
pkgname=mathgraph
pkgver=4.9
pkgrel=71
pkgdesc="Simple maths drawer"
arch=('any')

url=('http://www.mathgraph32.org/')

install=${pkgname}.install
license=('GPL')
depends=('java-environment')
source=("http://www.mathgraph32.org/IMG/zip/mathgraph32jarexecutablev49$pkgrel.zip"
	"${pkgname}.desktop")
md5sums=('ec8dd47b72ed2459c0162887f48d8f08'
         '5f867d58de2577498c040b9cc537d63c')

package() {
  cd "${srcdir}"
  
  install -d ${pkgdir}/usr/share/applications/
  install -d "$pkgdir/opt/mathgraph"
  install -d "${pkgdir}/usr/bin"

  cp -r Helpfra "$pkgdir/opt/mathgraph/"

  install -m644 ${pkgname}.desktop ${pkgdir}/usr/share/applications/

  install -m644 MathGraph32.jar "$pkgdir/opt/${pkgname}"

  echo "#!/bin/bash 
java -jar /opt/mathgraph/MathGraph32.jar" > "${pkgdir}/usr/bin/${pkgname}"
  chmod +x "${pkgdir}/usr/bin/${pkgname}"

}

