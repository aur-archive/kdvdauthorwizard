# Contributor: Andrea Scarpino <andrea@archlinux.org>
# Contributor: Georg Grabler (STiAT) <ggrabler@gmail.com>
# Contributor: DaNiMoTh <jjdanimoth@gmail.com>

pkgname=kdvdauthorwizard
pkgver=1.4.6
pkgrel=4
pkgdesc="A very simple and nice wizard app for authoring DVDs with menu and stuff, based on kommander"
arch=('i686' 'x86_64')
url="http://sourceforge.net/projects/dvdauthorwizard"
license=('GPL')
depends=('kdelibs3' 'imagemagick' 'dvdauthor' 'transcode' 'mjpegtools' 'mplayer' 'sox' 'bc')
replace=('dvdauthorwizard')
source=(http://downloads.sourceforge.net/dvdauthorwizard/DVDAuthorWizard-$pkgver.tar.bz2)
md5sums=('2998a159c515c6dd67b4da7af2810e52')

build() {
  cd $srcdir/DVDAuthorWizard-$pkgver
  install -d $pkgdir/opt/kde/share/applications/kde
  ./inst.sh ./ $pkgdir/opt/kde
  sed -ie 's/'${startdir//\//\\\/}'\/pkg//' $pkgdir/opt/kde/share/applications/kde/KDVDAuthoringWizard.desktop
}
