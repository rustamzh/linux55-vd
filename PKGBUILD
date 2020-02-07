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
_sub=2
kernelbase=${_basekernel}${_kernelname}
pkgver=${_basekernel}.${_sub}
pkgrel=2
_archpatch=20200205
arch=('x86_64')
url="http://www.kernel.org/"
license=('GPL2')
makedepends=('xmlto' 'docbook-xsl' 'kmod' 'inetutils' 'bc' 'elfutils' 'git')
options=('!strip')
source=(https://cdn.kernel.org/pub/linux/kernel/v5.x/linux-${pkgver}.tar.{xz,sign}
		# the main kernel config files
		'config.x86_64' 'config.vd' 'x509.genkey' "${pkgbase}.preset"
		# Prepatch from stable-queue
		#
		# ARCH Patches
		0001-arch-patches-${_archpatch}.patch::https://raw.githubusercontent.com/sirlucjan/kernel-patches/master/5.5/arch-patches-v7/0001-arch-patches.patch
		# MANJARO Patches
		0001-i2c-nuvoton-nc677x-hwmon-driver.patch
		0002-amdgpu-nonupstream-navi10-vfio-reset.patch
		# amdgpu
		#
		# BMQ scheduler
		#0001-bmq-linux55-20200126.patch::https://gitlab.com/alfredchen/bmq/raw/master/5.5/bmq_v5.5-r0.patch
		# sirlucjan
		#0001-futex-steam-fsync.patch::https://raw.githubusercontent.com/sirlucjan/kernel-patches/master/5.5/futex-patches-sep/0001-futex-Split-key-setup-from-key-queue-locking-and-rea.patch
		#0002-futex-steam-fsync.patch::https://raw.githubusercontent.com/sirlucjan/kernel-patches/master/5.5/futex-patches-sep/0002-futex-Implement-mechanism-to-wait-on-any-of-several-.patch
		#0003-futex-steam-fsync.patch::https://raw.githubusercontent.com/sirlucjan/kernel-patches/master/5.5/futex-patches-sep/0003-futex-Change-WAIT_MULTIPLE-opcode-to-31.patch
		0001-enable-O3-opt-for-all-archs.patch::https://raw.githubusercontent.com/sirlucjan/kernel-patches/master/5.5/cpu-patches-sep/0002-init-Kconfig-enable-O3-for-all-arches.patch
		# Clear Linux
		0001-clearlinux-tweak-intel-cpuidle.patch::https://raw.githubusercontent.com/clearlinux-pkgs/linux/master/0106-intel_idle-tweak-cpuidle-cstates.patch
		0002-clearlinux-add-config-opt-for-raid6-bench.patch::https://raw.githubusercontent.com/clearlinux-pkgs/linux/master/0109-raid6-add-Kconfig-option-to-skip-raid6-benchmarking.patch
		0003-clearlinux-init-ata-before-graphics.patch::https://raw.githubusercontent.com/clearlinux-pkgs/linux/master/0110-Initialize-ata-before-graphics.patch
		# steam futex
		0001-futex-steam-fsync.patch::https://gitlab.collabora.com/krisman/linux/commit/40ccab595e3dc54e474c1942162d5b678ff62f4c.diff
		0002-futex-steam-fsync.patch::https://gitlab.collabora.com/krisman/linux/commit/4576c43d6bcc275b6576f94f322519782ee621f8.diff
		0003-futex-steam-fsync.patch::https://gitlab.collabora.com/krisman/linux/commit/464c38516d56872d009f7b0e3bfdab363011e4fe.diff
		0004-futex-steam-fsync.patch::https://gitlab.collabora.com/krisman/linux/commit/3efc9c50ad64cb234fae91d430c4fba391bf1024.diff
		# vd
		0001-tune-vm-and-vfs-settings.patch
		0002-tune-cfs-scheduler.patch
		0003-optimise-module-compression.patch
		0004-tune-cpufreq-ondemand.patch
		0005-cpu-optimisations-graysky.patch
		0006-hwmon-56-backports.patch
		0007-ext4-for-fscrypt-56-backports.patch
		0008-fscrypt-56-backports.patch
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

sha256sums=('24f5f383b0337374f160723bcf3bf679c75cb5bd3fd0824a56998e47c04ef99e'
            'SKIP'
            'c88af29e587fb769b1902966800212079920435871d96cc9bbfbaab3a2880dc8'
            'b0467d5b02dc2c2722dfe72e1c8ba78b1c4943d69cd913cefebad28830626412'
            'ab010dc5ef6ce85d352956e5996d242246ecd0912b30f0b72025c38eadff8cd5'
            '47ec1e67dbd355a9cfa457a9c9a796d756c7159194d36917ab453e20a60114e3'
            'a01bc61cacb32bb71c4d0257000595dbb4d0f3efa498b9d5b8263a1b8c5ca70f'
            '0556859a8168c8f7da9af8e2059d33216d9e5378d2cac70ca54c5ff843fa5add'
            '7a2758f86dd1339f0f1801de2dbea059b55bf3648e240878b11e6d6890d3089c'
            '1c949aa5ca3beb4c84eccf57806d6cbe88c83b1cb79941002bc4b4954543f796'
            '88b5597753b01f90f77b99580943263969902ffc084972f8843e0659fdd5eb8f'
            '47d26eb8a2ec74b3684ab61837ecfcdad5cdc40722ca01a32684dfdd3775fafc'
            'b4a3d140bc93e4d224570c0f6b87c40c64148571588064858fcdc9f2406feeaa'
            '4cefd83b24f6c3a7d9e86075649d00c28305c52e6492b67ad32fca6a42ed8d39'
            '2c901cb8975284fb4c5d2b18455eb24a47272f716305425d1c70a38dfd1c8935'
            '68d11fd871015bce86924e90bd15e6adc243f2b3a0ae4c48a57852b17e45b15c'
            'cd8ec9de797e7700b6dd7d560e7f94ba202c8ffbfce8cbad1dfaad8d959662b7'
            '725d6693af00daf0a1e2fe8042249dfd16b90bb3f72e5cb841b9e4f7b82e4b7d'
            '58fd33be8d9ab594a01f1da5858567ac7ce8d3e44e0f2f3682e9104c4fb07514'
            '4b5d20022693ff63450fae6646b07caf00e0a97be49526995cad0365bc9269b6'
            '97f59d09ef55ea8a3634ea426fdc5db0591f77cca14cfe2db49176f71af80037'
            'cc739c9c9f7ce08e6bbc161b8232208bbc00820342a32fb1f69bff6326ae1370'
            'edfff1acfc374cb01c28c464e5a4feaa8b54f6ece3be02d71ca9cde3da0a909e'
            '516aba4e5547f912d9ca8471727dcc1b8ddc2bec2053eab44cfa7aeaa4aa2a5b'
            'aeea1112bff861ad5c6bb1b90393463b2141517c6d32e8a68b43729380ebea42'
            'b63220b9cb8295852838a0a4faccc3a6aead7f044a65df3f4945e502afbd0440'
            'f470403d798e300eaf321a97aad2141561324c4c5658500b64a2029e7e521a08'
            '67067a67fb75193b3608ab61fdca94228f74b2b360cf277bdfe6f7561658c9f4')

export KBUILD_BUILD_USER=manjaro
export KBUILD_BUILD_HOST=systemd-run

prepare() {
  local TBOLD=$(tput bold)
  local TNORMAL=$(tput sgr0)
  cd "${srcdir}/linux-${pkgver}"

  # add latest fixes from stable queue, if needed
  # http://git.kernel.org/?p=linux/kernel/git/stable/stable-queue.git
  # enable only if you have "gen-stable-queue-patch.sh" executed before
  #patch -Np1 -i "${srcdir}/prepatch-${_basekernel}`date +%Y%m%d`"

  printf '\n'
  msg2 "APPLYING PATCHES"

  # apply patch from the source array (should be a pacman feature)
  local filename filename2
  for filename in "${source[@]}"; do
  	if [[ "$filename" =~ \.patch$ || "$filename" =~ \.diff$ ]]; then
		filename="${filename%%::*}"
		filename2="${filename#*-}"
        	echo -e "\n---- Applying patch ${TBOLD}${filename2%%.*}${TNORMAL}:"
        	patch -Np1 -i "$srcdir/${filename}"
  	fi
  done

  # kernel config
  printf '\n'
  msg2 "KERNEL CONFIGURATION"
  local _config
  echo "---- Select configuration file:"
  echo "${TBOLD}1)${TNORMAL} Manjaro default"
  echo "${TBOLD}2)${TNORMAL} x570/x270"
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
    cat ../x509.genkey > ./certs/x509.genkey
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
  [[ $NCONFIG = "y" ]] && make nconfig

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
  [[ -f ./certs/vd55-kernel-key.pem ]] && rm ./certs/vd55-kernel-key.pem

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

