# $FreeBSD$

PROG=	pkg
SRCS=	pkg.c dns_utils.c config.c
MAN=	pkg.7

CONFS=		HardenedBSD.conf HardenedBSD.tor.conf
CONFSDIR=	/etc/pkg
CONFSMODE=	644

CFLAGS+=-I${SRCTOP}/contrib/libucl/include
.PATH:	${SRCTOP}/contrib/libucl/include
LIBADD=	archive fetch ucl sbuf crypto ssl util

.include <bsd.prog.mk>
