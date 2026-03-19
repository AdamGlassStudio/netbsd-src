#	$NetBSD: Makefile,v 1.21 2025/09/23 20:12:10 rillig Exp $

.include <bsd.own.mk>
.include "${NETBSDSRCDIR}/distrib/common/Makefile.distrib"

SUBDIR=		ramdisk .WAIT ramdisk-kernel .WAIT floppy cdroms liveimage
TARGETS+=	release

release: check_RELEASEDIR .WAIT ${DESTDIR}/usr/mdec/boot
	${RELEASE_INSTALL} ${DESTDIR}/usr/mdec/boot \
	    ${RELEASEDIR}/${RELEASEMACHINEDIR}/installation/netboot
# XXX boot.mop skipped — mopcopy crashes on Clang-compiled boot ELF

iso_image: .MAKE
	${MAKEDIRTARGET} cdroms iso_image

live_image: .MAKE
	${MAKEDIRTARGET} liveimage live_image

.include <bsd.subdir.mk>
