# AArch64 multi-platform
# Maintainer: Dan Johansen <strit@manjaro.org>
# Contributor: Kevin Mihelich <kevin@archlinuxarm.org>
# Contributor: Dragan Simic <dsimic@buserror.io>

pkgbase=linux
pkgver=5.17.5
pkgrel=2
_newversion=false
_stopbuild=false     # Will also stop if ${_newversion} is true
_srcname="linux-${pkgver/%.0/}"
_kernelname="${pkgbase#linux}"
_desc="AArch64 multi-platform"
arch=('aarch64')
url="http://www.kernel.org/"
license=('GPL2')
makedepends=('xmlto' 'docbook-xsl' 'kmod' 'inetutils' 'bc' 'git' 'dtc')
options=('!strip')
source=("http://www.kernel.org/pub/linux/kernel/v5.x/${_srcname}.tar.xz"
        '1001-arm64-dts-allwinner-add-hdmi-sound-to-pine-devices.patch'            # A64-based devices
        '1002-arm64-dts-allwinner-add-ohci-ehci-to-h5-nanopi.patch'                # Nanopi Neo Plus 2
        '1003-drm-bridge-analogix_dp-Add-enable_psr-param.patch'                   # Pinebook Pro;  From list: https://patchwork.kernel.org/project/dri-devel/patch/20200626033023.24214-2-shawn@anastas.io/
        '1004-gpu-drm-add-new-display-resolution-2560x1440.patch'                  # Odroid
        '1005-panfrost-Silence-Panfrost-gem-shrinker-loggin.patch'                 # Panfrost
        '1006-arm64-dts-rockchip-Add-Firefly-Station-p1-support.patch'             # Firefly Station P1
        '1007-drm-rockchip-add-support-for-modeline-32MHz-e.patch'                 # DP Alt Mode
        '1008-rk3399-rp64-pcie-Reimplement-rockchip-PCIe-bus-scan-delay.patch'     # RockPro64
        '1009-drm-meson-encoder-add-YUV422-output-support.patch'                   # Meson G12B
        '1010-arm64-dts-amlogic-add-initial-Beelink-GT1-Ultimate-dev.patch'        # Beelink GT1 Ultimate
        '1011-arm64-dts-amlogic-add-meson-g12b-ugoos-am6-plus.patch'               # Meson Ugoos
        '1012-drm-panfrost-scheduler-improvements.patch'                           # Panfrost;  Will be submitted upstream by the author
        '1013-arm64-dts-rockchip-Add-PCIe-bus-scan-delay-to-RockPr.patch'          # RockPro64
        '1014-drm-rockchip-support-gamma-control-on-RK3399.patch'                  # RK3399 VOP;  From list: https://patchwork.kernel.org/project/linux-arm-kernel/cover/20211019215843.42718-1-sigmaris@gmail.com/
        '1015-arm64-dts-rockchip-switch-to-hs200-on-rockpi4.patch'                 # Radxa Rock Pi 4;  Temporary hotfix, not for upstreaming
        '1016-arm64-dts-meson-remove-CPU-opps-below-1GHz-for-G12B-boards.patch'    # AMLogic [1/2];  From list: https://patchwork.kernel.org/project/linux-amlogic/patch/20220210100638.19130-2-christianshewitt@gmail.com/
        '1017-arm64-dts-meson-remove-CPU-opps-below-1GHz-for-SM1-boards.patch'     # AMLogic [2/2];  From list: https://patchwork.kernel.org/project/linux-amlogic/patch/20220210100638.19130-3-christianshewitt@gmail.com/
        '1018-arm64-dts-rockchip-Add-PCIe-bus-scan-delay-to-Rock-P.patch'          # Radxa Rock Pi 4
        '2001-Bluetooth-Add-new-quirk-for-broken-local-ext-features.patch'         # Bluetooth;  From list: https://patchwork.kernel.org/project/bluetooth/patch/20200705195110.405139-2-anarsoul@gmail.com/
        '2002-Bluetooth-btrtl-add-support-for-the-RTL8723CS.patch'                 # Bluetooth;  From list: https://patchwork.kernel.org/project/bluetooth/patch/20200705195110.405139-3-anarsoul@gmail.com/
        '2003-arm64-allwinner-a64-enable-Bluetooth-On-Pinebook.patch'              # Bluetooth;  From list: https://patchwork.kernel.org/project/bluetooth/patch/20200705195110.405139-4-anarsoul@gmail.com/
        '2004-arm64-dts-allwinner-enable-bluetooth-pinetab-pinepho.patch'          # Bluetooth;  The PinePhone part is in linux-next
        '2005-staging-add-rtl8723cs-driver.patch'                                  # Realtek WiFi;  Not upstreamable
        '2006-arm64-dts-allwinner-pinetab-add-accelerometer.patch'                 # PineTab Accelerometer
        '2007-arm64-dts-allwinner-pinetab-enable-jack-detection.patch'             # PineTab Audio
        '2008-brcmfmac-USB-probing-provides-no-board-type.patch'                   # Bluetooth;  Will be submitted upstream by the author
        '2009-dts-rockchip-Adapt-and-adopt-Type-C-support-from-Pin.patch'          # RockPro64 DP Alt Mode;  Not upstreamable
        '3170-arm64-dts-rk3399-pinebook-pro-Fix-USB-PD-charging.patch'             # Third set of patches: START
        '3172-arm64-dts-rk3399-pinebook-pro-Improve-Type-C-support.patch'          # Pinebook Pro Type-C patches from megous; original patch numbers found
        '3174-arm64-dts-rk3399-pinebook-pro-Remove-redundant-pinct.patch'          # on https://xff.cz/kernels/5.17/patches/ are retained, with just the first
        '3178-arm64-dts-rk3399-pinebook-pro-Don-t-allow-usb2-phy-d.patch'          # digit changed from 0 to 3, to make tracking easier
        '3339-drm-rockchip-cdn-dp-Disable-CDN-DP-on-disconnect.patch'
        '3355-usb-typec-fusb302-Set-the-current-before-enabling-pu.patch'
        '3359-usb-typec-fusb302-Update-VBUS-state-even-if-VBUS-int.patch'
        '3361-usb-typec-fusb302-Add-OF-extcon-support.patch'
        '3362-usb-typec-fusb302-Fix-register-definitions.patch'
        '3363-usb-typec-fusb302-Clear-interrupts-before-we-start-t.patch'
        '3364-usb-typec-typec-extcon-Add-typec-extcon-bridge-drive.patch'
        '3365-phy-rockchip-typec-Make-sure-the-plug-orientation-is.patch'
        '3372-phy-rockchip-inno-usb2-More-robust-charger-detection.patch'
        '3373-usb-typec-extcon-Don-t-touch-charger-proprties.patch'                # Third set of patches: END
        'config'
        'linux.preset'
        '60-linux.hook'
        '90-linux.hook')
md5sums=('2d9d725a716d27c82ea31d2b4e802158'
         '9aa0591c2d601a104d664a802a44728c'
         'e6fe272dc95a1c0a8f871924699fea16'
         '9f27b2a05eaeb1995fc0fcf6a8b923c4'
         '6f592c11f6adc1de0f06e5d18f8c2862'
         'f8f0b124c741be61d86bea8d44e875f9'
         '564136ab1c75b6dc67be02b54e695ae5'
         '66fae3fc96f0a478a56ff11632f3ef70'
         '245858f26512dfc48adbf509b6fc8364'
         '47ebd261e31fe881abafee88c9d33767'
         '8f4816a1ed98f80eebad49b6446427a9'
         '1b92d7617e60d3c525a4b18ab4351185'
         '140b727650029bf2d99f2d176f0876d8'
         '28982d87c45ed8f5aab966d82f8455d8'
         '19e2279811700cd8aa4ab326603d2f61'
         'a0f649f78c857a01e1680b89b58b05eb'
         '5f88754771166cd2d95d7bc3911cacca'
         'ee8eb5a23404c879fcfd09e5b7c124b8'
         'a0cf3209d3f856522ef14c4618837ae7'
         '372260658bc5fe55ee9b5690d8f67cb9'
         'a100d32aa6c345290061d2a773bf1232'
         '9510821113c122f91f47b9d0f7ca7264'
         'a74fcfa1e085a3a99dcf4f214c1ca65a'
         '256243b5df86300025b1f0b13cd03838'
         'd0fd6bd627223d4c9fc001ffff9df401'
         'f79300740a7350d2d24ab5e120831b52'
         'd2654df7fc87e5c874505a2d98cbce1c'
         '3d1c9ff232929189de8df70614304e13'
         '5e893acf3d94e12b34b8cff473c26218'
         'ac41d6c08c54c55d13c8fe894475ad65'
         '78cef676142df1365bba76957c3d3568'
         'dcc69b0564188ba62de6b70a4e3cd3cf'
         'f11053894ecba7af407caf3a72de4d7f'
         '6692e09bdea6e156290e22f54e1dc205'
         '2f4bd9db5c8f2d5625d3ff0cb46839c2'
         'e50f6fa84cf825cf6d0905a661bdcc42'
         '1b9950b3c76a0e43230fa37edd1dd80a'
         '55568672d443c4db1438f081e9fbcd92'
         '2b4e7d963ce6cc53518a3f6a2b14c30e'
         '482a6974207197cff14e77a61f66a810'
         'a76a46e31f4229e7c4349f90ac36601b'
         '04eec4b27d9c26f6d53317100fbab7fb'
         'ce52543b5f8dd0c175fdc0c22f591deb'
         '86d4a35722b5410e3b29fc92dae15d4b'
         'ce6c81ad1ad1f8b333fd6077d47abdaf'
         '3dc88030a8f2f5a5f97266d99b149f77')

prepare() {
  apply_patches() {
      local PATCH
      for PATCH in "${source[@]}"; do
          PATCH="${PATCH%%::*}"
          PATCH="${PATCH##*/}"
          [[ ${PATCH} = $1*.patch ]] || continue
          msg2 "Applying patch: ${PATCH}..."
          patch -N -p1 < "../${PATCH}"
      done
  }

  cd ${_srcname}

  # Assorted Manjaro ARM patches
  apply_patches 1

  # Assorted Pinebook, PinePhone and PineTab patches
  apply_patches 2

  # Pinebook Pro Type-C patches
  apply_patches 3

  # Apply our kernel configuration
  cat "${srcdir}/config" > ./.config

  # Add pkgrel to extraversion
  sed -ri "s|^(EXTRAVERSION =)(.*)|\1 \2-${pkgrel}|" Makefile

  # Don't run depmod on "make install", we'll do that ourselves in packaging
  sed -i '2iexit 0' scripts/depmod.sh
}

build() {
  cd ${_srcname}

  # Get the kernel version
  if [[ "${_newversion}" = false ]]; then
    make prepare
  fi

  # Configure the kernel; adjust the line below to your choice
  # or simply manually edit the ".config" file
  if [[ "${_newversion}" = true ]]; then
    make menuconfig   # CLI menu for configuration
  fi
  #make nconfig       # New CLI menu for configuration
  #make xconfig       # X-based configuration
  #make oldconfig     # Using old config from previous kernel version

  # Stash the configuration (use with new major kernel version)
  if [[ "${_newversion}" = true ]]; then
    cp ./.config /var/tmp/${pkgbase}.config
  fi

  # Stop here, which is useful to configure the kernel
  if [[ "${_newversion}" = true || "${_stopbuild}" = true ]]; then
    msg "Stopping build"
    return 1
  fi

  # Enable to create an all-inclusive build
  #yes "" | make config

  # Build the kernel and the modules
  unset LDFLAGS
  make ${MAKEFLAGS} Image modules

  # Generate device tree blobs with symbols to support
  # applying device tree overlays in U-Boot
  make ${MAKEFLAGS} DTC_FLAGS="-@" dtbs
}

_package() {
  pkgdesc="The Linux Kernel and modules - ${_desc}"
  depends=('coreutils' 'linux-firmware' 'kmod' 'initramfs')
  optdepends=('crda: to set the correct wireless channels of your country')
  provides=('kernel26' "linux=${pkgver}")
  conflicts=('kernel26' 'linux')
  replaces=('linux-armv8' 'linux-aarch64')
  backup=("etc/mkinitcpio.d/${pkgbase}.preset")
  install=${pkgname}.install

  cd ${_srcname}

  KARCH=arm64

  # get kernel version
  _kernver="$(make kernelrelease)"
  _basekernel=${_kernver%%-*}
  _basekernel=${_basekernel%.*}

  mkdir -p "${pkgdir}"/{boot,usr/lib/modules}
  make INSTALL_MOD_PATH="${pkgdir}/usr" modules_install
  make INSTALL_DTBS_PATH="${pkgdir}/boot/dtbs" dtbs_install
  cp arch/$KARCH/boot/Image "${pkgdir}/boot"

  # make room for external modules
  local _extramodules="extramodules-${_basekernel}${_kernelname}"
  ln -s "../${_extramodules}" "${pkgdir}/usr/lib/modules/${_kernver}/extramodules"

  # add real version for building modules and running depmod from hook
  echo "${_kernver}" |
    install -Dm644 /dev/stdin "${pkgdir}/usr/lib/modules/${_extramodules}/version"

  # remove build and source links
  rm "${pkgdir}"/usr/lib/modules/${_kernver}/{source,build}

  # now we call depmod...
  depmod -b "${pkgdir}/usr" -F System.map "${_kernver}"

  # sed expression for following substitutions
  local _subst="
    s|%PKGBASE%|${pkgbase}|g
    s|%KERNVER%|${_kernver}|g
    s|%EXTRAMODULES%|${_extramodules}|g
  "

  # install mkinitcpio preset file
  sed "${_subst}" ../linux.preset |
    install -Dm644 /dev/stdin "${pkgdir}/etc/mkinitcpio.d/${pkgbase}.preset"

  # install pacman hooks
  sed "${_subst}" ../60-linux.hook |
    install -Dm644 /dev/stdin "${pkgdir}/usr/share/libalpm/hooks/60-${pkgbase}.hook"
  sed "${_subst}" ../90-linux.hook |
    install -Dm644 /dev/stdin "${pkgdir}/usr/share/libalpm/hooks/90-${pkgbase}.hook"
}

_package-headers() {
  pkgdesc="Header files and scripts for building modules for linux kernel - ${_desc}"
  provides=("linux-headers=${pkgver}")
  conflicts=('linux-headers')
  replaces=('linux-aarch64-headers')

  cd ${_srcname}
  local _builddir="${pkgdir}/usr/lib/modules/${_kernver}/build"

  install -Dt "${_builddir}" -m644 Makefile .config Module.symvers
  install -Dt "${_builddir}/kernel" -m644 kernel/Makefile

  mkdir "${_builddir}/.tmp_versions"

  cp -t "${_builddir}" -a include scripts

  install -Dt "${_builddir}/arch/${KARCH}" -m644 arch/${KARCH}/Makefile
  install -Dt "${_builddir}/arch/${KARCH}/kernel" -m644 arch/${KARCH}/kernel/asm-offsets.s
  install -Dt "${_builddir}" -m644 vmlinux 

  cp -t "${_builddir}/arch/${KARCH}" -a arch/${KARCH}/include
  mkdir -p "${_builddir}/arch/arm"
  cp -t "${_builddir}/arch/arm" -a arch/arm/include

  install -Dt "${_builddir}/drivers/md" -m644 drivers/md/*.h
  install -Dt "${_builddir}/net/mac80211" -m644 net/mac80211/*.h

  # http://bugs.archlinux.org/task/13146
  install -Dt "${_builddir}/drivers/media/i2c" -m644 drivers/media/i2c/msp3400-driver.h

  # http://bugs.archlinux.org/task/20402
  install -Dt "${_builddir}/drivers/media/usb/dvb-usb" -m644 drivers/media/usb/dvb-usb/*.h
  install -Dt "${_builddir}/drivers/media/dvb-frontends" -m644 drivers/media/dvb-frontends/*.h
  install -Dt "${_builddir}/drivers/media/tuners" -m644 drivers/media/tuners/*.h

  # add xfs and shmem for aufs building
  mkdir -p "${_builddir}"/{fs/xfs,mm}

  # copy in Kconfig files
  find . -name Kconfig\* -exec install -Dm644 {} "${_builddir}/{}" \;

  # remove unneeded architectures
  local _arch
  for _arch in "${_builddir}"/arch/*/; do
    [[ ${_arch} == */${KARCH}/ || ${_arch} == */arm/ ]] && continue
    rm -r "${_arch}"
  done

  # remove documentation files
  rm -r "${_builddir}/Documentation"

  # remove now broken symlinks
  find -L "${_builddir}" -type l -printf 'Removing %P\n' -delete

  # strip scripts directory
  local file
  while read -rd '' file; do
    case "$(file -bi "$file")" in
      application/x-sharedlib\;*)      # Libraries (.so)
        strip $STRIP_SHARED "$file" ;;
      application/x-archive\;*)        # Libraries (.a)
        strip $STRIP_STATIC "$file" ;;
      application/x-executable\;*)     # Binaries
        strip $STRIP_BINARIES "$file" ;;
      application/x-pie-executable\;*) # Relocatable binaries
        strip $STRIP_SHARED "$file" ;;
    esac
  done < <(find "${_builddir}" -type f -perm -u+x ! -name vmlinux -print0 2>/dev/null)
  strip $STRIP_STATIC "${_builddir}/vmlinux"
  
  # remove unwanted files
  find ${_builddir} -name '*.orig' -delete
}

pkgname=("${pkgbase}" "${pkgbase}-headers")
for _p in ${pkgname[@]}; do
  eval "package_${_p}() {
    _package${_p#${pkgbase}}
  }"
done
