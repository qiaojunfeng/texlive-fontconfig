# Maintainer: Junfeng Qiao <qiaojunfeng at outlook.com>
# Contributor: 

# https://github.com/qiaojunfeng/texlive-fontconfig

pkgname=texlive-fontconfig
pkgdesc=""
pkgver=20190225
pkgrel=1
arch=(any)
url='https://github.com/qiaojunfeng/texlive-fontconfig'
license=(custom)
#depends=(fontconfig xorg-fonts-encodings xorg-mkfontscale xorg-mkfontdir)
depends=(texlive-bin)
#provides=(ttf-fangzheng)

package() {
    SRC=/etc/fonts/conf.avail/09-texlive-fonts.conf
    DEST=$(kpsewhich -var-value TEXMFSYSVAR)/fonts/conf/texlive-fontconfig.conf
    mkdir -p "$pkgdir/$(dirname $DEST)"
    #ln -s $SRC $pkgdir/$DEST
    cp $SRC $pkgdir/$DEST
    sed -i '4i  <dir>/usr/share/texmf-dist/fonts/opentype/public/fontawesome/</dir>' $pkgdir/$DEST
}

