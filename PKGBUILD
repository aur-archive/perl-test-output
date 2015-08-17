# Contributor: AUR Perl <aurperl@juster.info>
# Generator  : CPANPLUS::Dist::Arch 1.15

pkgname='perl-test-output'
pkgver='1.01'
pkgrel='1'
pkgdesc="Utilities to test STDOUT and STDERR messages."
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl>=5.006' 'perl-sub-exporter' 'perl-test-tester>=0.107')
makedepends=()
url='http://search.cpan.org/dist/Test-Output'
source=('http://search.cpan.org/CPAN/authors/id/B/BD/BDFOY/Test-Output-1.01.tar.gz')
md5sums=('bea1fe88e8725a5b3f7b66e69fc83dd2')
_distdir="${srcdir}/Test-Output-1.01"

build() {
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
      PERL_AUTOINSTALL=--skipdeps                            \
      PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
      PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
      MODULEBUILDRC=/dev/null

    cd "$_distdir"
    /usr/bin/perl Makefile.PL
    make
  )
}

check() {
  cd "$_distdir"
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""
    make test
  )
}

package() {
  cd "$_distdir"
  make install
  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:
