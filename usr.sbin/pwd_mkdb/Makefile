#	@(#)Makefile	8.1 (Berkeley) 6/6/93
# $FreeBSD$

.PATH: ${SRCTOP}/lib/libc/gen		# for pw_scan.c

PACKAGE=	runtime
PROG=	pwd_mkdb
MAN=	pwd_mkdb.8
SRCS=	pw_scan.c pwd_mkdb.c

CFI_OVERRIDE=-fno-sanitize=cfi-icall

CFLAGS+= -I${SRCTOP}/lib/libc/gen		# for pw_scan.h
.if defined(BOOTSTRAPPING)
CFLAGS+=-I${.CURDIR}/bootstrap
.endif

.include <bsd.prog.mk>
