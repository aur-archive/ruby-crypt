pkgname=ruby-crypt
_gemname=${pkgname#ruby-}
pkgver=1.1.4
pkgrel=1
pkgdesc="A pure-ruby implementation of a number of popular encryption algorithms."
arch=(any)
url="http://crypt.rubyforge.org/"
license=('unknown')
depends=('ruby')
source=(http://rubygems.org/downloads/${_gemname}-${pkgver}.gem)
noextract=(${_gemname}-${pkgver}.gem)
md5sums=('47a4db98f28398984846c5e8973d3e9c')

package() {
  cd "${srcdir}"
  export HOME=/tmp
  local _gemdir="$(ruby -rubygems -e'puts Gem.default_dir')"
  gem install --no-user-install --ignore-dependencies -i "${pkgdir}${_gemdir}" ${_gemname}-${pkgver}.gem
}
