pkgname=perl-http-message
pkgver=6.11
pkgrel=1
pkgdesc="HTTP style messages"
arch=('x86_64')
url='http://search.cpan.org/dist/HTTP-Message'
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl' 'perl-encode-locale' 'perl-http-date' 'perl-lwp-mediatypes' 'perl-uri'
         'perl-io-html')
conflicts=('perl-libwww<6')
source=("http://search.cpan.org/CPAN/authors/id/E/ET/ETHER/HTTP-Message-$pkgver.tar.gz")
md5sums=('4ed7add10daea3ab30abfeab6d03872f')

build() {
  cd HTTP-Message-$pkgver
  perl Makefile.PL INSTALLDIRS=vendor
  make
}

check() {
  cd HTTP-Message-$pkgver
  make test
}

package() {
  cd HTTP-Message-$pkgver
  make DESTDIR="$pkgdir" install
}
