# Maintainer: Joris Steyn <jorissteyn@gmail.com>
# Contributor: archeyDevil <archeydevil@gmail.com>

pkgname=vim-nerdtree-git
pkgver=4.2.0.112.gb0bb781
pkgrel=1
pkgdesc='A tree explorer plugin for vim'
arch=('any')
url="https://github.com/scrooloose/nerdtree"
license=('custom')
depends=('vim')
makedepends=('git')
groups=('vim-plugins')
install='vimdoc.install'
conflicts=('vim-nerdtree')
replaces=('vim-nerdtree')
provides=('vim-nerdtree')
source=('git://github.com/scrooloose/nerdtree.git#branch=master')
md5sums=('SKIP')

pkgver() {
  cd "$srcdir"/nerdtree
  git describe --tags --always | sed 's|-|.|g'
}

package() {
  install -d "${pkgdir}"/usr/share/vim/vimfiles/{doc,nerdtree_plugin,plugin,lib/nerdtree,syntax,autoload}

  install -D -m644 "${srcdir}"/nerdtree/doc/* \
    "${pkgdir}"/usr/share/vim/vimfiles/doc/

  install -D -m644 "${srcdir}"/nerdtree/nerdtree_plugin/* \
    "${pkgdir}"/usr/share/vim/vimfiles/nerdtree_plugin/

  install -D -m644 "${srcdir}"/nerdtree/lib/nerdtree/* \
    "${pkgdir}"/usr/share/vim/vimfiles/lib/nerdtree/

  install -D -m644 "${srcdir}"/nerdtree/plugin/* \
    "${pkgdir}"/usr/share/vim/vimfiles/plugin/

  install -D -m644 "${srcdir}"/nerdtree/syntax/* \
    "${pkgdir}"/usr/share/vim/vimfiles/syntax/

  install -D -m644 "${srcdir}"/nerdtree/autoload/* \
    "${pkgdir}"/usr/share/vim/vimfiles/autoload/
}

