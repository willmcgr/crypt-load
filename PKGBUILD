

pkgname=crypto-load
pkgver=2.e454a31
pkgrel=1
pkgdesc='Simple initcpio hook, probes cryptroot for sub-partitions.'
arch=('any')
license=('MIT')
depends=('mkinitcpio' 'parted')
source=(
        'crypt-load.hook'
        'crypt-load.install'
        'LICENSE'
        'README.md'
        )
md5sums=(
        'SKIP'
        'SKIP'
        'SKIP'
        'SKIP'
        )

pkgver(){
  printf "%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package(){
  install -Dm644 "${srcdir}/crypt-load.hook" \
      "${pkgdir}/usr/lib/initcpio/hooks/crypt-load"
  install -Dm644 "${srcdir}/crypt-load.install" \
      "${pkgdir}/usr/lib/initcpio/install/crypt-load"
  install -Dm644 "${srcdir}/LICENSE" \
      "${pkgdir}/usr/share/crypt-load/README.md"
  install -Dm644 "${srcdir}/README.md" \
      "${pkgdir}/usr/share/crypt-load/LICENSE"
}

