#	$NetBSD: Makefile,v 1.3 2004/11/14 11:26:48 yamt Exp $
#	$OpenBSD: Makefile,v 1.12 2004/04/25 19:24:52 deraadt Exp $

PROG=	authpf
MAN=	authpf.8
BINOWN= root
BINGRP= authpf
BINMODE= 6555
SRCS=	authpf.c
CFLAGS+= -Wall
COPTS.authpf.c+=	${${ACTIVE_CC} == "clang":? -Wno-error=fortify-source :}

.include <bsd.prog.mk>
