# Based on the file created for Arch Linux by:
# Tobias Powalowski <tpowa@archlinux.org>
# Thomas Baechler <thomas@archlinux.org>

# Maintainer: Philip Müller (x86_64) <philm@manjaro.org>
# Maintainer: Jonathon Fernyhough (i686) <jonathon@manjaro.org>
# Contributor: Helmut Stult <helmut[at]manjaro[dot]org>
# Maintainer (vd): torvic9

pkgbase=linux55-vd
pkgname=('linux55-vd' 'linux55-vd-headers')
_basekernel=5.5
_kernelname=-vd
_sub=0
kernelbase=${_basekernel}${_kernelname}
pkgver=${_basekernel}.${_sub}
pkgrel=1
_archpatch=20200130
arch=('x86_64')
url="http://www.kernel.org/"
license=('GPL2')
makedepends=('xmlto' 'docbook-xsl' 'kmod' 'inetutils' 'bc' 'elfutils' 'git')
options=('!strip')
source=(https://cdn.kernel.org/pub/linux/kernel/v5.x/linux-${_basekernel}.tar.{xz,sign}
		# the main kernel config files
		'config.x86_64' 'config.vd' 'x509.genkey' "${pkgbase}.preset"
		# Prepatch from stable-queue
		#
		# ARCH Patches
		0001-arch-patches-${_archpatch}.patch::https://raw.githubusercontent.com/sirlucjan/kernel-patches/master/5.5/arch-patches-v2/0001-arch-patches.patch
		# MANJARO Patches
		0001-i2c-nuvoton-nc677x-hwmon-driver.patch
		0002-amdgpu-nonupstream-navi10-vfio-reset.patch
		# amdgpu
		#
		# BMQ scheduler
		#0001-bmq-linux55-20200126.patch::https://gitlab.com/alfredchen/bmq/raw/master/5.5/bmq_v5.5-r0.patch
		# sirlucjan
		0001-futex-steam-fsync.patch::https://raw.githubusercontent.com/sirlucjan/kernel-patches/master/5.5/futex-patches-sep/0001-futex-Split-key-setup-from-key-queue-locking-and-rea.patch
		0002-futex-steam-fsync.patch::https://raw.githubusercontent.com/sirlucjan/kernel-patches/master/5.5/futex-patches-sep/0002-futex-Implement-mechanism-to-wait-on-any-of-several-.patch
		0003-futex-steam-fsync.patch::https://raw.githubusercontent.com/sirlucjan/kernel-patches/master/5.5/futex-patches-sep/0003-futex-Change-WAIT_MULTIPLE-opcode-to-31.patch
		0001-enable-O3-opt-for-all-archs.patch::https://raw.githubusercontent.com/sirlucjan/kernel-patches/master/5.5/cpu-patches-sep/0002-init-Kconfig-enable-O3-for-all-arches.patch
		# Clear Linux
		0001-clearlinux-tweak-intel-cpuidle.patch::https://raw.githubusercontent.com/clearlinux-pkgs/linux/master/0106-intel_idle-tweak-cpuidle-cstates.patch
		0002-clearlinux-add-config-opt-for-raid6-bench.patch::https://raw.githubusercontent.com/clearlinux-pkgs/linux/master/0109-raid6-add-Kconfig-option-to-skip-raid6-benchmarking.patch
		0003-clearlinux-init-ata-before-graphics.patch::https://raw.githubusercontent.com/clearlinux-pkgs/linux/master/0110-Initialize-ata-before-graphics.patch
		# vd
		0001-tune-vm-and-vfs-settings.patch
		0002-tune-cfs-scheduler.patch
		0003-optimise-module-compression.patch
		0004-tune-cpufreq-ondemand.patch
		0005-cpu-optimisations-graysky.patch
		0006-hwmon-56-backports.patch
		0007-fscrypt-56-backports.patch
		# hho
		#
		# cfs/sched tweaks
		0001-sched-dont-skip-remote-tick-for-idle-cpus.patch
		0002-sched-update-nohz-load-in-remote-tick.patch
		0003-sched-optimize-select_idle_core.patch
)

validpgpkeys=(
  'ABAF11C65A2970B130ABE3C479BE3E4300411886'  # Linus Torvalds
  '647F28654894E3BD457199BE38DBBDC86092693E'  # Greg Kroah-Hartman
)

sha256sums=('a6fbd4ee903c128367892c2393ee0d9657b6ed3ea90016d4dc6f1f6da20b2330'
            'SKIP'
            'c88af29e587fb769b1902966800212079920435871d96cc9bbfbaab3a2880dc8'
            '6f3373cceecc2e93b76d9b8ccd5c975423ea906eec7c0a4cfd723a59c2882636'
            'ab010dc5ef6ce85d352956e5996d242246ecd0912b30f0b72025c38eadff8cd5'
            'c14f60f37c5ef16d104aaa05fdc470f8d6d341181f5370b92918c283728e5625'
            '15a2ec0128ee1910b13c841bda7f90172b6731bfce4fba9d685bfb2333a3d85e'
            '0556859a8168c8f7da9af8e2059d33216d9e5378d2cac70ca54c5ff843fa5add'
            '7a2758f86dd1339f0f1801de2dbea059b55bf3648e240878b11e6d6890d3089c'
            'fd1f34cf87e72ccd6070590028ad34e12dc42285637a0c61894680cb81d4fb88'
            '9660f0d31bdc5718b7fde41015898f67dce86602886585848d6300dfce2542db'
            'cd228e4b62cab5679c93cd0eda5d96d570f1b3ba84340eddd2d049f2a07eef9d'
            '1c949aa5ca3beb4c84eccf57806d6cbe88c83b1cb79941002bc4b4954543f796'
            '88b5597753b01f90f77b99580943263969902ffc084972f8843e0659fdd5eb8f'
            '47d26eb8a2ec74b3684ab61837ecfcdad5cdc40722ca01a32684dfdd3775fafc'
            'b4a3d140bc93e4d224570c0f6b87c40c64148571588064858fcdc9f2406feeaa'
            '725d6693af00daf0a1e2fe8042249dfd16b90bb3f72e5cb841b9e4f7b82e4b7d'
            '58fd33be8d9ab594a01f1da5858567ac7ce8d3e44e0f2f3682e9104c4fb07514'
            '4b5d20022693ff63450fae6646b07caf00e0a97be49526995cad0365bc9269b6'
            '4281dfd457e93d39220bc3462a80a56b0b1b9f50987a59c0c4352338d70b7b71'
            'cc739c9c9f7ce08e6bbc161b8232208bbc00820342a32fb1f69bff6326ae1370'
            '342fc1d096324b92f69a27b4ec8e9b1e82ab87ae3042b0bd95f3b97820f98895'
            'aeea1112bff861ad5c6bb1b90393463b2141517c6d32e8a68b43729380ebea42'
            'b63220b9cb8295852838a0a4faccc3a6aead7f044a65df3f4945e502afbd0440'
            'f470403d798e300eaf321a97aad2141561324c4c5658500b64a2029e7e521a08'
            '67067a67fb75193b3608ab61fdca94228f74b2b360cf277bdfe6f7561658c9f4')

export KBUILD_BUILD_USER=systemd-run
export KBUILD_BUILD_HOST=manjaro

prepare() {
  local TBOLD=$(tput bold)
  local TNORMAL=$(tput sgr0)
  cd "${srcdir}/linux-${_basekernel}"

  # add latest fixes from stable queue, if needed
  # http://git.kernel.org/?p=linux/kernel/git/stable/stable-queue.git
  # enable only if you have "gen-stable-queue-patch.sh" executed before
  #patch -Np1 -i "${srcdir}/prepatch-${_basekernel}`date +%Y%m%d`"

  printf '\n'
  msg2 "APPLYING PATCHES"

  # apply patch from the source array (should be a pacman feature)
  local filename filename2
  for filename in "${source[@]}"; do
  	if [[ "$filename" =~ \.patch$ ]]; then
		filename="${filename%%::*}"
		filename2="${filename#*-}"
        	echo -e "\n---- Applying patch ${TBOLD}${filename2%%.*}${TNORMAL}:"
        	patch -Np1 -i "$srcdir/${filename}"
  	fi
  done

  cat ../x509.genkey > ./certs/x509.genkey

  # kernel config
  printf '\n'
  msg2 "KERNEL CONFIGURATION"
  local _config
  echo "---- Select configuration file:"
  echo "${TBOLD}1)${TNORMAL} Manjaro default"
  echo "${TBOLD}2)${TNORMAL} vd default"
  while true ; do
  	read -p "Enter number (1-5): " _config
	  case ${_config} in
		1) cat ../config.x86_64 > ./.config && break ;;
		2) cat ../config.vd > ./.config && break ;;
		*) echo "Please enter a number (1-5)!" && continue ;;
  	  esac
  done

  # add key
  printf '\n'
  msg2 "KERNEL KEY GENERATION"
  read -p "---- Enter the full path to the key if you have one, else enter 'n': " UCHOICE
  if [[ ${UCHOICE} != "n" ]]; then
    if [[ -f ${UCHOICE} ]]; then
      cat ${UCHOICE} > ./certs/vd55-kernel-key.pem || exit 2
    else
      echo "Path does not exist. Aborting..." ; exit 2
    fi
  else
    sed -i 's/vd55\-kernel\-key/signing\_key/' ./.config || exit 2
  fi

  if [ "${_kernelname}" != "" ]; then
    sed -i "s|CONFIG_LOCALVERSION=.*|CONFIG_LOCALVERSION=\"${_kernelname}\"|g" ./.config
    sed -i "s|CONFIG_LOCALVERSION_AUTO=.*|CONFIG_LOCALVERSION_AUTO=n|" ./.config
  fi

  # set patchlevel to 4
  #sed -ri "s|^(PATCHLEVEL =).*|\1 4|" Makefile

  # set extraversion to pkgrel
  sed -ri "s|^(EXTRAVERSION =).*|\1 -${pkgrel}|" Makefile

  # don't run depmod on 'make install'. We'll do this ourselves in packaging
  sed -i '2iexit 0' scripts/depmod.sh

  # get kernel version
  make prepare
  make -s kernelrelease > version
  printf '\n'
  msg2 "Prepared %s version %s" "$pkgbase" "$(<version)"
  read -p "---- Enter 'y' for nconfig: " NCONFIG
  if [[ $NCONFIG = "y" ]] ; then make nconfig ; fi

  # rewrite configuration
  yes "" | make config >/dev/null
}

build() {
  cd "${srcdir}/linux-${pkgver}"

  # build!
  make ${MAKEFLAGS} LOCALVERSION= bzImage modules
}

package_linux55-vd() {
  pkgdesc="The ${pkgbase/linux/Linux} vd kernel and modules"
  depends=('coreutils' 'linux-firmware' 'kmod' 'mkinitcpio>=27')
  optdepends=('crda: to set the correct wireless channels of your country')
  provides=("linux=${pkgver}")

  cd "${srcdir}/linux-${pkgver}"

  KARCH=x86

  local kernver="$(<version)"
  local modulesdir="$pkgdir/usr/lib/modules/$kernver"

  mkdir -p "${pkgdir}"/{boot,usr/lib/modules}
  printf '\n'
  msg2 "Installing modules..."
  make LOCALVERSION= INSTALL_MOD_PATH="${pkgdir}/usr" modules_install

  # systemd expects to find the kernel here to allow hibernation
  # https://github.com/systemd/systemd/commit/edda44605f06a41fb86b7ab8128dcf99161d2344
  install -Dm644 "$(make -s image_name)" "$modulesdir/vmlinuz"

  # Used by mkinitcpio to name the kernel
  echo "${pkgbase}" | install -Dm644 /dev/stdin "$modulesdir/pkgbase"
  echo "${kernelbase}-${CARCH}" | install -Dm644 /dev/stdin "$modulesdir/kernelbase"

  # add kernel version
  echo "${pkgver}-${pkgrel}${_kernelname} x64" > "${pkgdir}/boot/${pkgbase}-${CARCH}.kver"

  # make room for external modules
  local _extramodules="extramodules-${kernelbase}"
  ln -s "../${_extramodules}" "$modulesdir/extramodules"

  # add real version for building modules and running depmod from hook
  echo "${kernver}" |
    install -Dm644 /dev/stdin "${pkgdir}/usr/lib/modules/${_extramodules}/version"

  # now we call depmod...
  printf '\n'
  msg2 "Running depmod..."
  depmod -v -b "${pkgdir}/usr" -F System.map "$kernver"

  # remove build and source links
  rm $modulesdir/source
  rm $modulesdir/build

  # Fixing permissions
  printf '\n'
  msg2 "Fixing permissions..."
  chmod -Rc u=rwX,go=rX "$pkgdir"

  # add vmlinux
  #install -Dt "$modulesdir/build" -m644 vmlinux

  # add mkinitcpio preset (not strictly needed)
  install -Dm644 "$srcdir/${pkgbase}.preset" "$pkgdir/etc/mkinitcpio.d/${pkgbase}.preset"
}

package_linux55-vd-headers() {
  pkgdesc="Header files and scripts for building modules for ${pkgbase/linux/Linux} vd kernel"
  provides=("linux-headers=$pkgver")

  cd "${srcdir}/linux-${pkgver}"
  local kernver="$(<version)"
  local _builddir="${pkgdir}/usr/lib/modules/${kernver}/build"

  printf '\n'
  msg2 "Installing headers..."
  install -Dt "${_builddir}" -m644 Makefile .config Module.symvers System.map || exit 32
  install -Dt "${_builddir}/kernel" -m644 kernel/Makefile

  mkdir "${_builddir}/.tmp_versions"

  cp -t "${_builddir}" -a include scripts

  install -Dt "${_builddir}/arch/${KARCH}" -m644 "arch/${KARCH}/Makefile"
  install -Dt "${_builddir}/arch/${KARCH}/kernel" -m644 "arch/${KARCH}/kernel/asm-offsets.s"
  #install -Dt "${_builddir}/arch/${KARCH}/kernel" -m644 "arch/${KARCH}/kernel/macros.s"

  cp -t "${_builddir}/arch/${KARCH}" -a "arch/${KARCH}/include"

  # add objtool for external module building and enabled VALIDATION_STACK option
  install -Dt "${_builddir}/tools/objtool" tools/objtool/objtool

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

  # remove unneeded stuff
  printf '\n'
  msg2 "Removing unneeded files..."
  # remove unneeded architectures
  local _arch
  for _arch in "${_builddir}"/arch/*/; do
    [[ ${_arch} == */x86/ ]] && continue
    rm -r "${_arch}"
  done

  # remove files already in linux-docs package
  rm -r "${_builddir}/Documentation"

  # remove broken symlinks
  find -L "${_builddir}" -type l -printf 'Removing %P\n' -delete

  # remove loose objects"
  find "${_builddir}" -type f -name '*.o' -printf 'Removing %P\n' -delete

  # strip scripts directory
  printf '\n'
  msg2 "Stripping build tools..."
  local file
  while read -rd '' file; do
    case "$(file -bi "$file")" in
      application/x-sharedlib\;*)      # Libraries (.so)
        strip -v $STRIP_SHARED "$file" ;;
      application/x-archive\;*)        # Libraries (.a)
        strip -v $STRIP_STATIC "$file" ;;
      application/x-executable\;*)     # Binaries
        strip -v $STRIP_BINARIES "$file" ;;
      application/x-pie-executable\;*) # Relocatable binaries
        strip -v $STRIP_SHARED "$file" ;;
    esac
  done < <(find "${_builddir}" -type f -perm -u+x ! -name vmlinux -print0)

  # Fix permissions
  printf '\n'
  msg2 "Fixing permissions..."
  chmod -Rc u=rwX,go=rX "${pkgdir}"
}

