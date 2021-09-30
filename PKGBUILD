# AArch64 multi-platform
# Maintainer: Dan Johansen <strit@manjaro.org>
# Contributor: Kevin Mihelich <kevin@archlinuxarm.org>

pkgbase=linux
_srcname=linux-5.14
_kernelname=${pkgbase#linux}
_desc="AArch64 multi-platform"
pkgver=5.14.9
pkgrel=1
arch=('aarch64')
url="http://www.kernel.org/"
license=('GPL2')
makedepends=('xmlto' 'docbook-xsl' 'kmod' 'inetutils' 'bc' 'git' 'dtc')
options=('!strip')
source=("http://www.kernel.org/pub/linux/kernel/v5.x/${_srcname}.tar.xz"
        "http://www.kernel.org/pub/linux/kernel/v5.x/patch-${pkgver}.xz"
        '0001-net-smsc95xx-Allow-mac-address-to-be-set-as-a-parame.patch'
        '0002-arm64-dts-amlogic-add-support-for-Radxa-Zero.patch' #Applied in linux-next
        '0003-arm64-dts-allwinner-add-hdmi-sound-to-pine-devices.patch'
        '0004-arm64-dts-allwinner-add-ohci-ehci-to-h5-nanopi.patch'
        '0005-drm-bridge-analogix_dp-Add-enable_psr-param.patch'
        '0006-gpu-drm-add-new-display-resolution-2560x1440.patch'
        '0007-nuumio-panfrost-Silence-Panfrost-gem-shrinker-loggin.patch'
        '0008-arm64-dts-rockchip-Add-Firefly-Station-p1-support.patch'
        '0009-typec-displayport-some-devices-have-pin-assignments-reversed.patch' #Not upstreamable
        '0010-usb-typec-add-extcon-to-tcpm.patch' #Not upstreamable #requires cdn_dp to be enabled
        '0011-arm64-rockchip-add-DP-ALT-rockpro64.patch' #Not upstreamable
        '0012-ayufan-drm-rockchip-add-support-for-modeline-32MHz-e.patch'
        '0013-rk3399-rp64-pcie-Reimplement-rockchip-PCIe-bus-scan-delay.patch'
        '0014-phy-rockchip-typec-Set-extcon-capabilities.patch' #Needs tcpm patch 0012 #Not upstreamable
        '0015-usb-typec-altmodes-displayport-Add-hacky-generic-altmode.patch' #Not upstreamable
        '0016-arm64-dts-rockchip-add-typec-extcon-hack.patch' #Not upstreamable
        '0017-arm64-dts-rockchip-setup-USB-type-c-port-as-dual-data-role.patch' #Applied in linux-next
        '0018-drm-meson-add-YUV422-output-support.patch'
        '0019-arm64-dts-meson-add-initial-Beelink-GT1-Ultimate-dev.patch'
        '0020-add-ugoos-device.patch'
        '0021-drm-panfrost-Handle-failure-in-panfrost_job_hw_submit.patch'
        '0022-arm64-dts-rockchip-Add-pcie-bus-scan-delay-to-rockpr.patch'
        '0023-Revert-net-stmmac-dwmac-rk-fix-unbalanced-pm_runtime.patch'
        '0001-Bluetooth-Add-new-quirk-for-broken-local-ext-features.patch'
        '0002-Bluetooth-btrtl-add-support-for-the-RTL8723CS.patch'
        '0003-arm64-allwinner-a64-enable-Bluetooth-On-Pinebook.patch'
        '0004-arm64-dts-allwinner-enable-bluetooth-pinetab-pinepho.patch' #Pinephone part is in linux-next
        '0005-staging-add-rtl8723cs-driver.patch' #Not upstreamable
        '0006-pinetab-accelerometer.patch'
        '0007-enable-jack-detection-pinetab.patch'
        '0008-enable-hdmi-output-pinetab.patch'
        '0009-drm-panel-Adjust-sync-values-for-Feixin-K101-IM2BYL02-panel.patch' #Submitted upstream https://patchwork.kernel.org/project/dri-devel/patch/20210818214818.298089-1-strit@manjaro.org/
        '0001-arm64-dts-rockchip-Add-quartz64-a-dts-from-linux-nex.patch' #Applied in linux-next
        '0002-fixes-and-enablement-for-rk356x.patch' #Applied in linux-next
        '0003-Rockchip-I2S-TDM-controller.patch'
        '0004-Patches-to-update-for-rockchip-spdif.patch' #Applied in linux-next
        '0005-gpio-rockchip-driver.patch' #Applied in linux-next
        '0006-PCI-rockchip-Add-Rockchip-RK356X-host-controller-driver.patch' #Applied in linux-next
        '0007-rockchip-io-domain.patch' #Applied in linux-next
        '0008-dt-bindings-iio-adc-rockchip-saradc-add-description-for-rk3568.patch' #Applied in linux-next
        '0009-power-supply-Add-Support-for-RK817-Charger.patch'
        '0010-dt-bindings-pwm-rockchip-add-description-for-rk3568.patch'
        '0011-phy-rockchip-inno-usb2-support-rk356x-usb2phy.patch'
        'config'
        'linux.preset'
        '60-linux.hook'
        '90-linux.hook')
md5sums=('a082ef5748b813abca0649dab8be5f52'
         '64e3961a575595f67cb7abea4ad28ba4'
         '9e6b7f44db105fef525d715213dce7cf'
         '754cf09a858498e1d98b44baa043a196'
         '0d47dea87f03bf36262171e01889f832'
         'e6fe272dc95a1c0a8f871924699fea16'
         '9f27b2a05eaeb1995fc0fcf6a8b923c4'
         '6f592c11f6adc1de0f06e5d18f8c2862'
         'f8f0b124c741be61d86bea8d44e875f9'
         '073296b5eba7daf6d707c21abbfc49ce'
         'a033be22c23afb1d5daeeeb21353185d'
         'c02e0fbd88085970a667e86c15fdf364'
         '09fc19ac5c51e2839ca56248ccf6323a'
         '66fae3fc96f0a478a56ff11632f3ef70'
         '245858f26512dfc48adbf509b6fc8364'
         '252b4dbd2d0f560b6d254f29dd5b0f5f'
         'ab9c0c25e2b7272fca3caf491b7dc89c'
         'c706ccdf118f4146e7ca35808d819b8a'
         'bb500ee93275583d5ba3d11842e09735'
         '469417b64e6a2bf65bd74c6d9cad2040'
         'c41b101c033ac487c15298bc5a9e95cd'
         '1b92d7617e60d3c525a4b18ab4351185'
         'a90a366662357233db7022f8a1e7ac46'
         '6bb2d84857359016b5e0878cf2fc50cc'
         '4d1c5ad859cf3f22c0c9f7903d6d761c'
         'cf64831f27bb47da29e708b7243bb340'
         'e3f53e07612939729afaa4dd7ef7f7ce'
         '9510821113c122f91f47b9d0f7ca7264'
         'a74fcfa1e085a3a99dcf4f214c1ca65a'
         '4d3adc0015b0e6a9ff88e170e96d3d06'
         'd0fd6bd627223d4c9fc001ffff9df401'
         'f79300740a7350d2d24ab5e120831b52'
         '979a787cf84bef9c60da78e72ec96550'
         'b05068c0ae9edbdb39d6678117e8cb05'
         'bae82c4f8f8ee360df7695537d542e0e'
         'a1c29fc4c7ea01af094a5a90c675620b'
         'e8adada273680ff94b3f2c5a0e8dce31'
         'ea47c01b9dd9a10c1d3332108f6a4868'
         '6338a3a993e86692e1817e1f498bd210'
         'f2203a951a7c3f2444e6618e49da0b93'
         'bca5c0228958767b018b612fb10a6a6d'
         'dec0be99fe374fad3a8650aaf672596e'
         '7659fe53cc58b9a7ed615b49719f7066'
         'ae85e433bc4fd787c20a4df0d07d528b'
         '15b2d6fd96df0a070a8f1b4fc5399b8b'
         '8e9eb69572db2f4c772cc387cc91fc4a'
         '86d4a35722b5410e3b29fc92dae15d4b'
         'ce6c81ad1ad1f8b333fd6077d47abdaf'
         '3dc88030a8f2f5a5f97266d99b149f77')

prepare() {
  cd ${_srcname}

  # add upstream patch
  patch -Np1 -i "${srcdir}/patch-${pkgver}"

  # ALARM patches
  patch -Np1 -i "${srcdir}/0001-net-smsc95xx-Allow-mac-address-to-be-set-as-a-parame.patch"             #All
  
  # Manjaro ARM Patches
  patch -Np1 -i "${srcdir}/0002-arm64-dts-amlogic-add-support-for-Radxa-Zero.patch"                     #Radxa Zero
  patch -Np1 -i "${srcdir}/0003-arm64-dts-allwinner-add-hdmi-sound-to-pine-devices.patch"               #Pine64
  patch -Np1 -i "${srcdir}/0004-arm64-dts-allwinner-add-ohci-ehci-to-h5-nanopi.patch"                   #Nanopi Neo Plus 2
  patch -Np1 -i "${srcdir}/0005-drm-bridge-analogix_dp-Add-enable_psr-param.patch"                      #Pinebook Pro
  patch -Np1 -i "${srcdir}/0006-gpu-drm-add-new-display-resolution-2560x1440.patch"                     #Odroid
  patch -Np1 -i "${srcdir}/0007-nuumio-panfrost-Silence-Panfrost-gem-shrinker-loggin.patch"             #Panfrost
  patch -Np1 -i "${srcdir}/0008-arm64-dts-rockchip-Add-Firefly-Station-p1-support.patch"                #Firelfy Station P1
  patch -Np1 -i "${srcdir}/0009-typec-displayport-some-devices-have-pin-assignments-reversed.patch"     #DP Alt Mode
  patch -Np1 -i "${srcdir}/0010-usb-typec-add-extcon-to-tcpm.patch"                                     #DP Alt Mode
  patch -Np1 -i "${srcdir}/0011-arm64-rockchip-add-DP-ALT-rockpro64.patch"                              #DP Alt mode - RockPro64
  patch -Np1 -i "${srcdir}/0012-ayufan-drm-rockchip-add-support-for-modeline-32MHz-e.patch"             #DP Alt mode
  patch -Np1 -i "${srcdir}/0013-rk3399-rp64-pcie-Reimplement-rockchip-PCIe-bus-scan-delay.patch"        #RockPro64
  patch -Np1 -i "${srcdir}/0014-phy-rockchip-typec-Set-extcon-capabilities.patch"                       #DP Alt mode
  patch -Np1 -i "${srcdir}/0015-usb-typec-altmodes-displayport-Add-hacky-generic-altmode.patch"         #DP Alt mode
  patch -Np1 -i "${srcdir}/0018-drm-meson-add-YUV422-output-support.patch"                              #G12B
  patch -Np1 -i "${srcdir}/0019-arm64-dts-meson-add-initial-Beelink-GT1-Ultimate-dev.patch"             #Beelink
  patch -Np1 -i "${srcdir}/0020-add-ugoos-device.patch"                                                 #Ugoos
  patch -Np1 -i "${srcdir}/0021-drm-panfrost-Handle-failure-in-panfrost_job_hw_submit.patch"            #AMLogic
  patch -Np1 -i "${srcdir}/0022-arm64-dts-rockchip-Add-pcie-bus-scan-delay-to-rockpr.patch"             #RockPro64
  patch -Np1 -i "${srcdir}/0023-Revert-net-stmmac-dwmac-rk-fix-unbalanced-pm_runtime.patch"             #Fix ethernet on RK3399
  
  # Pinebook Pro patches
  patch -Np1 -i "${srcdir}/0016-arm64-dts-rockchip-add-typec-extcon-hack.patch"                         #DP Alt mode
  patch -Np1 -i "${srcdir}/0017-arm64-dts-rockchip-setup-USB-type-c-port-as-dual-data-role.patch"       #USB-C charging
  
  # Pinebook, PinePhone and PineTab patches
  patch -Np1 -i "${srcdir}/0001-Bluetooth-Add-new-quirk-for-broken-local-ext-features.patch"            #Bluetooth
  patch -Np1 -i "${srcdir}/0002-Bluetooth-btrtl-add-support-for-the-RTL8723CS.patch"                    #Bluetooth
  patch -Np1 -i "${srcdir}/0003-arm64-allwinner-a64-enable-Bluetooth-On-Pinebook.patch"                 #Bluetooth
  patch -Np1 -i "${srcdir}/0004-arm64-dts-allwinner-enable-bluetooth-pinetab-pinepho.patch"             #Bluetooth
  patch -Np1 -i "${srcdir}/0005-staging-add-rtl8723cs-driver.patch"                                     #Wifi
  patch -Np1 -i "${srcdir}/0006-pinetab-accelerometer.patch"                                            #accelerometer
  patch -Np1 -i "${srcdir}/0007-enable-jack-detection-pinetab.patch"                                    #Audio
  patch -Np1 -i "${srcdir}/0008-enable-hdmi-output-pinetab.patch"                                       #HDMI
  patch -Np1 -i "${srcdir}/0009-drm-panel-Adjust-sync-values-for-Feixin-K101-IM2BYL02-panel.patch"      #Display
  
  # Quartz64 development patches, will probably change alot
  #patch -Np1 -i "${srcdir}/0001-arm64-dts-rockchip-Add-quartz64-a-dts-from-linux-nex.patch"             #Main DTS
  #patch -Np1 -i "${srcdir}/0002-fixes-and-enablement-for-rk356x.patch"                                  #Fixes to DTS's
  #patch -Np1 -i "${srcdir}/0003-Rockchip-I2S-TDM-controller.patch"                                      #Analog audio
  #patch -Np1 -i "${srcdir}/0004-Patches-to-update-for-rockchip-spdif.patch"                             #Digital audio
  #patch -Np1 -i "${srcdir}/0005-gpio-rockchip-driver.patch"                                             #GPIO V8
  #patch -Np1 -i "${srcdir}/0006-PCI-rockchip-Add-Rockchip-RK356X-host-controller-driver.patch"          #PCIe
  #patch -Np1 -i "${srcdir}/0007-rockchip-io-domain.patch"                                               #IO Domain
  #patch -Np1 -i "${srcdir}/0008-dt-bindings-iio-adc-rockchip-saradc-add-description-for-rk3568.patch"   #Microphone
  #patch -Np1 -i "${srcdir}/0009-power-supply-Add-Support-for-RK817-Charger.patch"                       #Charger
  #patch -Np1 -i "${srcdir}/0010-dt-bindings-pwm-rockchip-add-description-for-rk3568.patch"              #PWM
  #patch -Np1 -i "${srcdir}/0011-phy-rockchip-inno-usb2-support-rk356x-usb2phy.patch"                    #USB2PHY
  
  cat "${srcdir}/config" > ./.config

  # add pkgrel to extraversion
  sed -ri "s|^(EXTRAVERSION =)(.*)|\1 \2-${pkgrel}|" Makefile

  # don't run depmod on 'make install'. We'll do this ourselves in packaging
  sed -i '2iexit 0' scripts/depmod.sh
}

build() {
  cd ${_srcname}

  # get kernel version
  make prepare

  # load configuration
  # Configure the kernel. Replace the line below with one of your choice.
  #make menuconfig # CLI menu for configuration
  #make nconfig # new CLI menu for configuration
  #make xconfig # X-based configuration
  #make oldconfig # using old config from previous kernel version
  # ... or manually edit .config

  # Copy back our configuration (use with new kernel version)
  #cp ./.config /var/tmp/${pkgbase}.config

  ####################
  # stop here
  # this is useful to configure the kernel
  #msg "Stopping build"
  #return 1
  ####################

  #yes "" | make config

  # build!
  unset LDFLAGS
  make ${MAKEFLAGS} Image modules
  # Generate device tree blobs with symbols to support applying device tree overlays in U-Boot
  make ${MAKEFLAGS} DTC_FLAGS="-@" dtbs
}

_package() {
  pkgdesc="The Linux Kernel and modules - ${_desc}"
  depends=('coreutils' 'linux-firmware' 'kmod' 'mkinitcpio>=0.7')
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

  # Fix permissions
  find -P "${_builddir}" -type f -print | xargs chmod 0644
  find -P "${_builddir}" -type d -print | xargs chmod 0755 
}

pkgname=("${pkgbase}" "${pkgbase}-headers")
for _p in ${pkgname[@]}; do
  eval "package_${_p}() {
    _package${_p#${pkgbase}}
  }"
done
