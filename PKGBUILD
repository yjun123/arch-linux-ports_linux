# Maintainer: Jan Alexander Steffens (heftig) <heftig@archlinux.org>

pkgbase=linux
pkgver=7.2.11.arch1
pkgrel=1
pkgdesc='Linux'
url='https://github.com/archlinux/linux'
arch=(
  aarch64
  x86_64
)
license=(GPL-2.0-only)
makedepends=(
  bc
  binutils
  cpio
  gettext
  glibc
  libelf
  libgcc
  openssl
  pahole
  perl
  python
  rust
  rust-bindgen
  rust-src
  tar
  xxhash
  xz
  zlib
  zstd

  # htmldocs
  graphviz
  imagemagick
  python-sphinx
  python-yaml
  texlive-latexextra
)
options=(
  !debug
  !strip
)
_srcname=linux-${pkgver%.*}
_srctag=v${pkgver%.*}-${pkgver##*.}
source=(
  https://cdn.kernel.org/pub/linux/kernel/v${pkgver%%.*}.x/${_srcname}.tar.{xz,sign}
  $url/releases/download/$_srctag/linux-$_srctag.patch.zst{,.sig}
  0000-mmc-pwrseq_simple-fix-probe-failure-when-CONFIG_RESE.patch
  0001-mmc-sdhci-of-dwcmshc-downgrade-HS200-HS400-clock-red.patch
  0002-dt-bindings-vendor-prefixes-Add-sunniwell-prefix.patch
  0003-dt-bindings-arm-rockchip-Add-Sunniwell-Z96A-Type-C-c.patch
  0004-arm64-dts-rockchip-Add-Sunniwell-Z96A-Type-C.patch
  0005-dt-bindings-sound-add-Everest-ES7202.patch
  0006-ASoC-codecs-add-support-for-Everest-ES7202-PDM-ADC.patch
  0007-arm64-dts-rockchip-rk3568-sunniwell-z96a-pd-add-ES72.patch
  0008-dt-bindings-display-rockchip-analogix-dp-add-RK3568-.patch
  0009-dt-bindings-phy-rockchip-add-RK3568-Naneng-eDP-PHY.patch
  0010-drm-bridge-analogix_dp-add-RK3568-eDP-device-type.patch
  0011-drm-rockchip-analogix_dp-add-RK3568-eDP-support.patch
  0012-phy-rockchip-add-RK3568-Naneng-eDP-PHY-driver.patch
  0013-drm-panel-edp-Add-BOE-NV140FHD-N43-panel.patch
  0014-arm64-dts-rockchip-rk3568-add-eDP-controller-and-PHY.patch
  0015-arm64-dts-rockchip-rk3568-sunniwell-z96a-pd-enable-e.patch
  0016-dt-bindings-vendor-prefixes-Add-southchip-prefix.patch
  0017-dt-bindings-mfd-bq25703a-Add-Southchip-SC8886S.patch
  0018-mfd-bq257xx-Add-support-for-Southchip-SC8886S.patch
  0019-power-supply-bq257xx-add-fuel-gauge-driver.patch
  0020-mfd-bq257xx-add-module-aliases-for-charger-and-regul.patch
  0021-power-supply-bq257xx-reprogram-charge-parameters-on-.patch
  0022-arm64-dts-rockchip-rk3568-sunniwell-z96a-pd-add-batt.patch
)
source_aarch64=(config.aarch64 config.sunniwell-z96a-typec)
source_x86_64=(config.x86_64)
validpgpkeys=(
  ABAF11C65A2970B130ABE3C479BE3E4300411886  # Linus Torvalds
  647F28654894E3BD457199BE38DBBDC86092693E  # Greg Kroah-Hartman
  83BC8889351B5DEBBB68416EB8AC08600F108CDF  # Jan Alexander Steffens (heftig)
)
sha256sums=('fd0fc479f983a8c05313f13e9c36330fe6651cf725396748c40d5cd93fa1e6a4'
            'SKIP'
            '741d473c4db335d97d9e1d9b8be9337090522550804fe6454ba336d21e580fd6'
            'SKIP'
            '18f261d19b0a63d52aeca933dc590523c9634615e852e53a720e7786b2f3b1a1'
            'aea1ca1db26d2dfd4c2ef71c2635708840fb4719310ac42fbfe228d1037583e5'
            '061bb3cb6466ffd3fa7f73c7589d5167784e09a204dcb8a0f31544b7ffcb959f'
            'e6781d0c5290907143ffab0b6fc91c8fb48fbabd9880a7c4b60a0b5f679076dd'
            '0f0ced8c85d9772461e2545115e81423bbc51afa3a8fa7fdcc81770025278e25'
            'e61b16d4e2901934f46eaaf99327dc55fb577da73de09403827b5c25dc01e823'
            '47ab991ab99fc32361abea477efb39ca2346e595a104a79907b81e08ac36258a'
            '984a9c3d304ca7478f3890836fedab2c71a1328d5e3c6135a405815e02ea5f67'
            '25aeea32c3dee98faf357aede8cc12edc5a4483f18539d699d016cbff5efb985'
            '9b75176e93c4a51b2d8f506930120242ceceffad26d818264730f0a0dd8a2c3d'
            '5091f19d0b6b466241d81588d3095be32ae6b53fbcc209fe405deaa64458fa85'
            '0c17d5614ee81a5933bfd86a333a526939e21507de053a160be4db0b06051598'
            'bfb2510a1571681661fd3fdd433b93150cdd28b2cfa806af72a0bffb83b2e566'
            '63c56746336d3552b7a86fc4428ccbbf1a297eef2dd8a6e355e8017ca7b5627e'
            'f9126db09797db23a5aeb064aa529e74660d00ac3d2b2343203481fde731ab3f'
            'b504896d92c2e69949b0162bbd079222a5ef50f80cc514a545920a7ec4b55819'
            'c282bc395a6bf78ce0e05e9408d27fd1691357c50b4c47233a6e56fac7aa20f7'
            'e09f93aa999a3df73cef0d904f34f4a0697920aa9ba46b94296397c2ffc29dce'
            '147a9e9af7ab53a1c99b7fe705b9167a77f889838b3862bbb285215237251a8f'
            '1f3dd2ef2c1d7aab99a046b875410347c9e1e1e86650fbd2383043d3b101da1b'
            '0507746ba9dde157821202a4927c58899728c0e97e798dd52f33009aa2598d83'
            'c5a59827e76e3f210072f6bef6efd288aa00aeba84883e9b960936e590e87bc4'
            'c014ab11a2b53f00a6a5418dfebe3f6e504813bdbe786afcf4ea3f8e47af0eb1')
sha256sums_aarch64=('5770111e938fee7df98346d640c97f28d698b9d926c93b92c71ad067c9d7cce4'
                    '8ec241081f74fa6ad2f2e931221c60da28ac347aba915ca81da9534bc11fdb14')
sha256sums_x86_64=('f16adcb6dc1dc241ea90e23ca920697d00e4618df1b72d914ff15bc55ab4051f')
b2sums=('36a455379876a3f452dce7347211ac34ddfda9a445b0b8c0ee92664429a8ea85d2f1a101126b6d748545aaf18e3534f8db53d6110952f3d5487d029ff0f9a800'
        'SKIP'
        '06f49715b71884a0cbad51ab4b526c1516926cb2429e7a6e485aa48ebf277811dec391ae2264501245654275a84af1df3780bf8bf8df755cf47670d6c9397703'
        'SKIP'
        'd83894ad713c88fd3d45af6ac8e10bc741092e5204a9a22e412d2cfdf4d3a2dce02d604fa5d1b582c7d458fdec212f6badfe9965d7038e38f4cf3afd5c28eade'
        '8c1a146693bbaad12603d79192615db3345b406b8a442e9edb096b7c1505f6ea0d8096d90ac0eec28f0ad6bb389b51e98d5e81105a6eedec92c4395e11126db1'
        'd3b523fae7bc13d08b86b81fa9f83073b40e1a9c02a7d7a5a18f00411786ea4ca7ab36c745963f8383fd6b7fd9e17a2468673cc6201974bc5101576e02848111'
        'c9c2e24a3070899dde5abde2e4a1b45b76a0f276d7d4d6442341b8f551f33e6eafb19356440d2134c8aa7191fde406fb2860d6e6d80ad18d6290b2eb47b94d28'
        '9863377e654f9e2d5efc2b3ec931b4fc608861bd1c2a87fe42fc0b3b37a1473498863dd302156a38b182d3a127b52229f5a7069d0ae1f0fdbfc265e434a094f0'
        '4ce59ef5d6b8c3987b340818cce56b7f45389aac9798d99644090d766a6a0558b7de0ddf7ef2e55c997064f1fc5295b5b9bbc4949e005710c18b63f7343688c1'
        'a50af2ece63f3244bcec5aa0cc6a3ff7e293161c8fd2c25a1389982deee53adca3f9d63ede7bdab8de1d50c302f244ae3c7f47b045a7ce8eae368863c4798ccc'
        'af510ccaba0d3a7aced4e6655f80ff90b9e408eaae4ff281ab0c12c88c52c3e962814bc2463ead702f281fbd39663ae837a676d22f37359d5d8b78f1f4ef1164'
        'e0b24e0ade1dab2de5d75f4f25e53c4d3d12c6c8945f49418d6915fdca69e00604a29ad17d6cba984c49dad3c6702540f2ce1fec4e3cef9f5f95b134dcf3e392'
        'cf887f570f2d33f862de48d4aa71473cf99dd53b97d00f57d6f7070f5da4663c08a19d93275d9f6de6b5487c688d7669bd029147992e69fb0730296b9c174236'
        '8ba2a4b1a3902eb4613379289efa5dd7603012a499d01fff205f1dc5eae5a502f266c32a79b27a5a018c4ae925eef8008f42af20eea83a841d6e3cb1c5cff9ed'
        'd117a6c379ac10db12eaca589c9bae0f4e06fe890dd9bc2a29d35b0d74ba177d2849508cb1027f336815b1918485e114dd5c9c459f31e4213c92dd6fae5249e8'
        '5e86225f122c850c45100a690505c4ec2ecaab25343e3d6a5367d65b93e2936f718225bf474817fc6e8a22f5d714806fad04e670b8458df0489b0374b75ff1a0'
        'dd5c31c982e2e9c9e608dc0851816e8e8c3d14b01facc6c5777c78b821fa12f0748c15b24644b0e1ccbe0a061031f7626b753ea232cd08d111335be8b8fe3e89'
        '39a0babc8d5a475e21d354b57aea7d9f7447cb238ca8a65ddfdf3f41dd2eb340f62d03c95a8e350fd66d592e74bde0b5649d6af516344b499814fcb57fb57ce3'
        '3a329a6065972b7434bba58b7a79f02fd0af18cce3523a27112bdfde186fd01bca7c4cb2ebe1cc5b12cf0d834117b3fccaf5f55f68ce32434c17834d18976304'
        '839abc686cc90fb244f2e0035b7a149eb70c8769aa4d295ed55453c342cd7d220cdfaf6a951353fcb64ccb007e9013b7380e2fed31ea07a73ad9bb5539069a52'
        'b56c42fc7369614ac79ed5824896c13362af5d5b13da70593b1f5a2c41859b18418ab65108b218ac6ee6d9bc6885eb362e95bf38cc76f9b776c02fbd51484b8f'
        '4ce39e2f2c94864222455cd07a3a689428144a089481ab510650f09235456fc5b00c18a73ddf4b0c050cd448d60b727a6373befb7d0a947b8bb17cc713928918'
        'f8ea7a881c0331c4149520a3d0d2e38c024914721834c0f81607d2acd27bd699f96dfd1ad488004acd3f4b8cc0571956c787371bb6298893f0bcd6e9d7727917'
        'cab30910e3fdd4cae44315cf7dbba2ede396aa88e97ffc9732ceedac4cbf4c4f8b0aeff759b5a9f2a7e5b2dc8d9840962f54d815a721a815f32723bb7ba6455e'
        '117a2de3bfd90f0db4b973b0ab9455b7a895e0ac57e25181dfeed326ccefa82405f828f05a90f4b596287064c183fc8963f603d422063fd837486033bf74542b'
        '3f95a5868dad83aee62a5994a0c16757cf4955aac20112cb7f7878ae86a975805d3d4e5838e00784623d9fe50c564241c9203c50c13debb84f27b94b3b144a7b')
b2sums_aarch64=('9ae5cb684e1232cbe65d57c2c585926767e73e3154468375d235c285d582f9fc51f6e5fe7fc67e9ee0ebb4cb59d92f3ee7dccb49463b93500629109865483ba0'
                '24dd5a4acfaeae372e7c3d88f807625091996d379d1793b3b9ae02434fb3d571a12cf253752da58e8ffdefd2c987ad607aa395939126dab1e0f8a2b286d679f6')
b2sums_x86_64=('58babcf7bed396598de1a7c010292aebb56b2c726f9d8d28344049646d5ed814489db0e22a4e62718e5e6dcc94c581858c17b235e88dc3263fa78934d2a84104')

# https://www.kernel.org/pub/linux/kernel/v7.x/sha256sums.asc

export KBUILD_BUILD_HOST=archlinux
export KBUILD_BUILD_USER=$pkgbase
export KBUILD_BUILD_TIMESTAMP="$(date -Ru${SOURCE_DATE_EPOCH:+d @$SOURCE_DATE_EPOCH})"

prepare() {
  cd $_srcname

  echo "Setting version..."
  echo "-$pkgrel" > localversion.10-pkgrel
  echo "${pkgbase#linux}" > localversion.20-pkgname

  local src
  for src in "${source[@]}"; do
    src="${src%%::*}"
    src="${src##*/}"
    src="${src%.zst}"
    [[ $src = *.patch ]] || continue
    echo "Applying patch $src..."
    patch -Np1 < "../$src"
  done

  echo "Setting config..."
  cp ../config.$CARCH .config
  declare -n configs="source_${CARCH}"
  local config
  for config in "${configs[@]:1}"; do
    ./scripts/kconfig/merge_config.sh -m .config ${srcdir}/$config
  done

  make olddefconfig
  diff -u ../config.$CARCH .config || :

  make -s kernelrelease > version
  echo "Prepared $pkgbase version $(<version)"
}

build() {
  cd $_srcname

  make htmldocs SPHINXOPTS=-QT &
  local pid_docs=$!

  make all
  make -C tools/bpf/bpftool vmlinux.h feature-clang-bpf-co-re=1
  wait $pid_docs
}

_package() {
  pkgdesc="The $pkgdesc kernel and modules"
  depends=(
    coreutils
    initramfs
    kmod
  )
  optdepends=(
    "$pkgbase-headers: headers and scripts for building modules"
    'linux-firmware: firmware images needed for some devices'
    'scx-scheds: to use sched-ext schedulers'
    'wireless-regdb: to set the correct wireless channels of your country'
  )
  optdepends_aarch64=(
    "$pkgbase-dtbs: device tree binaries"
  )
  provides=(
    KSMBD-MODULE
    NTSYNC-MODULE
    VIRTUALBOX-GUEST-MODULES
    WIREGUARD-MODULE
  )
  replaces=(
    virtualbox-guest-modules-arch
    wireguard-arch
  )

  cd $_srcname
  local modulesdir="$pkgdir/usr/lib/modules/$(<version)"

  echo "Installing boot image..."
  # systemd expects to find the kernel here to allow hibernation
  # https://github.com/systemd/systemd/commit/edda44605f06a41fb86b7ab8128dcf99161d2344
  install -Dm644 "$(make -s image_name)" "$modulesdir/vmlinuz"

  # Used by mkinitcpio to name the kernel
  echo "$pkgbase" | install -Dm644 /dev/stdin "$modulesdir/pkgbase"

  echo "Installing modules..."
  ZSTD_CLEVEL=19 make INSTALL_MOD_PATH="$pkgdir/usr" INSTALL_MOD_STRIP=1 \
    DEPMOD=/doesnt/exist modules_install  # Suppress depmod

  # remove build link
  rm "$modulesdir"/build
}

_package-headers() {
  pkgdesc="Headers and scripts for building modules for the $pkgdesc kernel"
  depends=(
    binutils
    glibc
    libelf
    libgcc
    openssl
    pahole
    xxhash
    zlib
    zstd
  )
  provides=(LINUX-HEADERS)

  cd $_srcname
  local builddir="$pkgdir/usr/lib/modules/$(<version)/build"

  local karch
  case $CARCH in
    aarch64) karch=arm64 ;;
    x86_64) karch=x86 ;;
    *) echo "Unknown CARCH $CARCH"; exit 1 ;;
  esac

  echo "Installing build files..."
  install -Dt "$builddir" -m644 .config Makefile Module.symvers System.map \
    localversion.* version vmlinux tools/bpf/bpftool/vmlinux.h
  install -Dt "$builddir/kernel" -m644 kernel/Makefile
  install -Dt "$builddir/arch/$karch" -m644 arch/$karch/Makefile
  cp -t "$builddir" -a scripts
  ln -srt "$builddir" "$builddir/scripts/gdb/vmlinux-gdb.py"

  if [[ $(scripts/config -s CONFIG_HAVE_STACK_VALIDATION) = y ]]; then
    install -Dt "$builddir/tools/objtool" tools/objtool/objtool
  fi

  if [[ $(scripts/config -s CONFIG_DEBUG_INFO_BTF_MODULES) = y ]]; then
    install -Dt "$builddir/tools/bpf/resolve_btfids" tools/bpf/resolve_btfids/resolve_btfids
  fi

  echo "Installing headers..."
  cp -t "$builddir" -a include
  cp -t "$builddir/arch/$karch" -a arch/$karch/include
  install -Dt "$builddir/arch/$karch/kernel" -m644 arch/$karch/kernel/asm-offsets.s

  install -Dt "$builddir/drivers/md" -m644 drivers/md/*.h
  install -Dt "$builddir/net/mac80211" -m644 net/mac80211/*.h

  # https://bugs.archlinux.org/task/13146
  install -Dt "$builddir/drivers/media/i2c" -m644 drivers/media/i2c/msp3400-driver.h

  # https://bugs.archlinux.org/task/20402
  install -Dt "$builddir/drivers/media/usb/dvb-usb" -m644 drivers/media/usb/dvb-usb/*.h
  install -Dt "$builddir/drivers/media/dvb-frontends" -m644 drivers/media/dvb-frontends/*.h
  install -Dt "$builddir/drivers/media/tuners" -m644 drivers/media/tuners/*.h

  # https://bugs.archlinux.org/task/71392
  install -Dt "$builddir/drivers/iio/common/hid-sensors" -m644 drivers/iio/common/hid-sensors/*.h

  echo "Installing KConfig files..."
  find . -name 'Kconfig*' -exec install -Dm644 {} "$builddir/{}" \;

  if [[ $(scripts/config -s CONFIG_RUST) = y ]]; then
    echo "Installing Rust files..."
    install -Dt "$builddir/rust" -m644 rust/*.rmeta
    install -Dt "$builddir/rust" rust/*.so
  fi

  echo "Installing unstripped VDSO..."
  make INSTALL_MOD_PATH="$pkgdir/usr" vdso_install \
    link=  # Suppress build-id symlinks

  echo "Removing unneeded architectures..."
  local arch
  for arch in "$builddir"/arch/*/; do
    [[ $arch = */$karch/ ]] && continue
    echo "Removing $(basename "$arch")"
    rm -r "$arch"
  done

  echo "Removing documentation..."
  rm -r "$builddir/Documentation"

  echo "Removing broken symlinks..."
  find -L "$builddir" -type l -printf 'Removing %P\n' -delete

  echo "Removing loose objects..."
  find "$builddir" -type f -name '*.o' -printf 'Removing %P\n' -delete

  echo "Stripping build tools..."
  local file
  while read -rd '' file; do
    case "$(file -Sib "$file")" in
      application/x-sharedlib\;*)      # Libraries (.so)
        strip -v $STRIP_SHARED "$file" ;;
      application/x-archive\;*)        # Libraries (.a)
        strip -v $STRIP_STATIC "$file" ;;
      application/x-executable\;*)     # Binaries
        strip -v $STRIP_BINARIES "$file" ;;
      application/x-pie-executable\;*) # Relocatable binaries
        strip -v $STRIP_SHARED "$file" ;;
    esac
  done < <(find "$builddir" -type f -perm -u+x ! -name vmlinux -print0)

  echo "Stripping vmlinux..."
  strip -v $STRIP_STATIC "$builddir/vmlinux"

  echo "Adding symlink..."
  mkdir -p "$pkgdir/usr/src"
  ln -sr "$builddir" "$pkgdir/usr/src/$pkgbase"
}

_package-docs() {
  pkgdesc="Documentation for the $pkgdesc kernel"

  cd $_srcname
  local builddir="$pkgdir/usr/lib/modules/$(<version)/build"

  echo "Installing documentation..."
  local src dst
  while read -rd '' src; do
    dst="${src#Documentation/}"
    dst="$builddir/Documentation/${dst#output/}"
    install -Dm644 "$src" "$dst"
  done < <(
    find Documentation \( -name '.*' -o -name __pycache__ \) -prune \
      -o \! -type d -print0
  )

  echo "Adding symlink..."
  mkdir -p "$pkgdir/usr/share/doc"
  ln -sr "$builddir/Documentation" "$pkgdir/usr/share/doc/$pkgbase"
}

_package-dtbs() {
  pkgdesc="Device tree binaries for the $pkgdesc kernel"
  arch=(aarch64)

  cd $_srcname
  local modulesdir="$pkgdir/usr/lib/modules/$(<version)"
  local dtbdir="$modulesdir/dtb"

  echo "Installing device tree binaries..."
  mkdir -p "$dtbdir"
  make INSTALL_DTBS_PATH="$dtbdir" dtbs_install
}

pkgname=(
  "$pkgbase"
  "$pkgbase-headers"
  "$pkgbase-docs"
  "$pkgbase-dtbs"
)
for _p in "${pkgname[@]}"; do
  eval "package_$_p() {
    $(declare -f "_package${_p#$pkgbase}")
    _package${_p#$pkgbase}
  }"
done

# vim:set ts=8 sts=2 sw=2 et:
