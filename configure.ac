AC_INIT([openpli-branding-module],[7.0])
AM_INIT_AUTOMAKE([dist-bzip2 foreign no-define tar-pax])
AC_CONFIG_HEADERS([enigma2-plugins-config.h])

# Silent rules are available since 1.11, but older versions
# are still in use. So don't use them unconditionally.
m4_ifdef([AM_SILENT_RULES], [AM_SILENT_RULES([yes])])

AC_USE_SYSTEM_EXTENSIONS
AC_SYS_LARGEFILE

AC_PROG_CC
AC_PROG_CXX
m4_ifdef([LT_INIT], [LT_INIT], [AC_PROG_LIBTOOL])
AC_CONFIG_MACRO_DIR([m4])

AC_CHECK_HEADERS([dbox/fp.h dbox/lcd-ks0713.h])

AC_PATH_PROG(MSGFMT, msgfmt, AC_MSG_ERROR(Could not find msgfmt))

AM_PATH_PYTHON
AX_PYTHON_DEVEL
AX_PTHREAD

AC_ARG_WITH(oever,
	[  --with-oever=NAME oe name [[7.2,...]]],
	[OE_VER="$withval"],[OE_VER=""])
AC_SUBST(OE_VER)
AC_DEFINE_UNQUOTED(OE_VER,"$OE_VER",[oe name])

AC_ARG_WITH(distro,
	[  --with-distro=NAME distro name [[openvision,...]]],
	[DISTRO="$withval"],[DISTRO=""])
AC_SUBST(DISTRO)
AC_DEFINE_UNQUOTED(DISTRO,"$DISTRO",[distro name])

AC_ARG_WITH(boxtype,
	[  --with-boxtype=NAME box type [[dm800,...]]],
	[BOXTYPE="$withval"],[BOXTYPE=""])
AC_SUBST(BOXTYPE)
AC_DEFINE_UNQUOTED(BOXTYPE,"$BOXTYPE",[box type])

AC_ARG_WITH(brandoem,
	[  --with-brandoem=NAME brand oem [[dreambox,...]]],
	[BRAND_OEM="$withval"],[BRAND_OEM=""])
AC_SUBST(BRAND_OEM)
AC_DEFINE_UNQUOTED(BRAND_OEM,"$BRAND_OEM",[brand oem])

AC_ARG_WITH(machinebrand,
	[  --with-machinebrand=NAME brand name [[dreambox,...]]],
	[MACHINE_BRAND="$withval"],[MACHINE_BRAND=""])
AC_SUBST(MACHINE_BRAND)
AC_DEFINE_UNQUOTED(MACHINE_BRAND,"$MACHINE_BRAND",[machine name])

AC_ARG_WITH(machinename,
	[  --with-machinename=NAME machine name [[dm800,...]]],
	[MACHINE_NAME="$withval"],[MACHINE_NAME=""])
AC_SUBST(MACHINE_NAME)
AC_DEFINE_UNQUOTED(MACHINE_NAME,"$MACHINE_NAME",[machine name])

AC_ARG_WITH(machinebuild,
	[  --with-machinebuild=NAME build name [[dm800,...]]],
	[MACHINE_BUILD="$withval"],[MACHINE_BUILD=""])
AC_SUBST(MACHINE_BUILD)
AC_DEFINE_UNQUOTED(MACHINE_BUILD,"$MACHINE_BUILD",[build name])

AC_ARG_WITH(machinemake,
	[  --with-machinemake=NAME build name [[dm800,...]]],
	[MACHINE_MAKE="$withval"],[MACHINE_MAKE=""])
AC_SUBST(MACHINE_MAKE)
AC_DEFINE_UNQUOTED(MACHINE_MAKE,"$MACHINE_MAKE",[build name])

AC_ARG_WITH(imageversion,
	[  --with-imageversion=NAME version number [[number,...]]],
	[IMAGEVERSION="$withval"],[IMAGEVERSION=""])
AC_SUBST(IMAGEVERSION)
AC_DEFINE_UNQUOTED(IMAGEVERSION,"$IMAGEVERSION",[version number])

AC_ARG_WITH(imagebuild,
	[  --with-imagebuild=NAME build number [[number,...]]],
	[IMAGEBUILD="$withval"],[IMAGEBUILD=""])
AC_SUBST(IMAGEBUILD)
AC_DEFINE_UNQUOTED(IMAGEBUILD,"$IMAGEBUILD",[build number])

AC_ARG_WITH(imagedevbuild,
	[  --with-imagedevbuild=NAME dev build number [[number,...]]],
	[IMAGEDEVBUILD="$withval"],[IMAGEDEVBUILD=""])
AC_SUBST(IMAGEDEVBUILD)
AC_DEFINE_UNQUOTED(IMAGEDEVBUILD,"$IMAGEDEVBUILD",[build number])

AC_ARG_WITH(imagetype,
	[  --with-imagetype=NAME imagetype name [[release,...]]],
	[DISTRO_TYPE="$withval"],[DISTRO_TYPE=""])
AC_SUBST(DISTRO_TYPE)
AC_DEFINE_UNQUOTED(DISTRO_TYPE,"$DISTRO_TYPE",[imagetype name])

AC_ARG_WITH(feedsurl,
	[  --with-feedsurl=NAME feeds url  [[628]]],
	[FEEDSURL="$withval"],[FEEDSURL=""])
AC_SUBST(FEEDSURL)
AC_DEFINE_UNQUOTED(FEEDSURL,"$FEEDSURL",[feeds url ])

AC_ARG_WITH(imagedir,
	[  --with-imagedir=NAME imagedir folder [[628]]],
	[IMAGEDIR="$withval"],[IMAGEDIR=""])
AC_SUBST(IMAGEDIR)
AC_DEFINE_UNQUOTED(IMAGEDIR,"$IMAGEDIR",[imagedir folder])

AC_ARG_WITH(imagefs,
	[  --with-imagefs=NAME imagefs folder [[628]]],
	[IMAGE_FSTYPES="$withval"],[IMAGE_FSTYPES=""])
AC_SUBST(IMAGE_FSTYPES)
AC_DEFINE_UNQUOTED(IMAGE_FSTYPES,"$IMAGE_FSTYPES",[imagefs folder])

AC_ARG_WITH(mtdbootfs,
	[  --with-mtdbootfs=NAME mtdbootfs number [[mmcblk0p4,...]]],
	[MTD_BOOTFS="$withval"],[MTD_BOOTFS=""])
AC_SUBST(MTD_BOOTFS)
AC_DEFINE_UNQUOTED(MTD_BOOTFS,"$MTD_BOOTFS",[mtdbootfs number])

AC_ARG_WITH(mtdrootfs,
	[  --with-mtdrootfs=NAME mtdrootfs number [[mmcblk0p19,...]]],
	[MTD_ROOTFS="$withval"],[MTD_ROOTFS=""])
AC_SUBST(MTD_ROOTFS)
AC_DEFINE_UNQUOTED(MTD_ROOTFS,"$MTD_ROOTFS",[mtdrootfs number])

AC_ARG_WITH(mtdkernel,
	[  --with-mtdkernel=NAME mtdkernel number [[mmcblk0p18,...]]],
	[MTD_KERNEL="$withval"],[MTD_KERNEL=""])
AC_SUBST(MTD_KERNEL)
AC_DEFINE_UNQUOTED(MTD_KERNEL,"$MTD_KERNEL",[mtdkernel number])

AC_ARG_WITH(rootfile,
	[  --with-rootfile=NAME rootfile name [[rootfs.tar.bz2,...]]],
	[ROOTFS_FILE="$withval"],[ROOTFS_FILE=""])
AC_SUBST(ROOTFS_FILE)
AC_DEFINE_UNQUOTED(ROOTFS_FILE,"$ROOTFS_FILE",[rootfile name])

AC_ARG_WITH(kernelfile,
	[  --with-kernelfile=NAME kernelfile name [[uImage,...]]],
	[KERNEL_FILE="$withval"],[KERNEL_FILE=""])
AC_SUBST(KERNEL_FILE)
AC_DEFINE_UNQUOTED(KERNEL_FILE,"$KERNEL_FILE",[kernelfile name])

AC_ARG_WITH(mkubifs,
	[  --with-mkubifs=NAME mkubifs number [[2048,...]]],
	[MKUBIFS_ARGS="$withval"],[MKUBIFS_ARGS=""])
AC_SUBST(MKUBIFS_ARGS)
AC_DEFINE_UNQUOTED(MKUBIFS_ARGS,"$MKUBIFS_ARGS",[mkubifs number])

AC_ARG_WITH(ubinize,
	[  --with-ubinize=NAME ubinize number [[2048,...]]],
	[UBINIZE_ARGS="$withval"],[UBINIZE_ARGS=""])
AC_SUBST(UBINIZE_ARGS)
AC_DEFINE_UNQUOTED(UBINIZE_ARGS,"$UBINIZE_ARGS",[ubinize number])

AC_ARG_WITH(arch,
	[  --with-arch=NAME arch name [[mips32el,...]]],
	[ARCH_TYPE="$withval"],[ARCH_TYPE=""])
AC_SUBST(ARCH_TYPE)
AC_DEFINE_UNQUOTED(ARCH_TYPE,"$ARCH_TYPE",[arch name])

AC_ARG_WITH(transcoding,
	[  --with-transcoding=NAME transcoding [[transcoding,...]]],
	[HAVE_TRANSCODING="$withval"],[HAVE_TRANSCODING="True"])
AC_SUBST(HAVE_TRANSCODING)
AC_DEFINE_UNQUOTED(HAVE_TRANSCODING,"$HAVE_TRANSCODING",[transcoding])

AC_ARG_WITH(multitranscoding,
	[  --with-multitranscoding=NAME multitranscoding [[multitranscoding,...]]],
	[HAVE_MULTITRANSCODING="$withval"],[HAVE_MULTITRANSCODING="True"])
AC_SUBST(HAVE_MULTITRANSCODING)
AC_DEFINE_UNQUOTED(HAVE_MULTITRANSCODING,"$HAVE_MULTITRANSCODING",[multitranscoding])

AC_ARG_WITH(debug,
	AS_HELP_STRING([--without-debug],[disable debugging code]),
	[with_debug="$withval"],[with_debug=""])
if test "$with_debug" = "yes"; then
	DEBUG_CFLAGS="-ggdb3"
	AC_DEFINE([DEBUG],[1],[Define to 1 to enable debugging code])
fi
AC_SUBST(DEBUG_CFLAGS)

AC_CONFIG_FILES([
Makefile
BoxBranding/Makefile
BoxBranding/lib/Makefile
])
AC_OUTPUT
