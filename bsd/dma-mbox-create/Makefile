#

version!=	sh ../../get-version.sh ../../VERSION

CFLAGS+= -I${.CURDIR}/../..
CFLAGS+= -DHAVE_REALLOCF -DHAVE_STRLCPY -DHAVE_GETPROGNAME
CFLAGS+= -DLIBEXEC_PATH='"${LIBEXEC}"' -DDMA_VERSION='"${version}"'
CFLAGS+= -DCONF_PATH='"${CONFDIR}"'

PROG=	dma-mbox-create
.PATH: ${.CURDIR}/../..
SRCS+=	dma-mbox-create.c
NOMAN=
MK_MAN=	no

PREFIX?=	/usr/local
LIBEXEC?=	${PREFIX}/libexec
CONFDIR?=	${PREFIX}/etc/dma

BINOWN= root
BINGRP= mail
BINMODE=4554

.include <bsd.prog.mk>
