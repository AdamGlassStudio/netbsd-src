#	$NetBSD: Makefile,v 1.7 2014/01/19 21:50:17 apb Exp $
#
.include <bsd.own.mk>

ATFFILE=	no
TESTSDIR=	${TESTSBASE}/lib/libcurses
TESTS_C+=	slave

PROG=	slave
NOMAN=	"true"
#MAN=	slave.7
SRCS=	slave.c commands.c curses_commands.c

CPPFLAGS+=	-I${.CURDIR} -I. -I${.CURDIR}/../director
LDADD+=		-lcurses -lterminfo -Wl,--no-fatal-warnings

COPTS.curses_commands.c += -Wno-format-nonliteral
COPTS.curses_commands.c += ${${ACTIVE_CC} == "clang":? -Wno-error=unused-but-set-parameter :}
CWARNFLAGS.clang+=	-Wno-format

.include <bsd.test.mk>
