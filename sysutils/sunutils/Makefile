# $OpenBSD$

V =		2018.09.26
COMMENT =	Sun-derived userland utilities
DISTNAME =	schily-${V:S/./-/g}
PKGNAME =	sunutils-${V}
EXTRACT_SUFX =	.tar.bz2
CATEGORIES =	sysutils

HOMEPAGE =	http://schilytools.sourceforge.net/
MAINTAINER =	Brian Callahan <bcallah@openbsd.org>

# CDDL
PERMIT_PACKAGE_CDROM =	Yes

MASTER_SITES =	${MASTER_SITE_SOURCEFORGE:=schilytools/}

#SEPARATE_BUILD =	Yes

USE_GMAKE =	Yes
MAKE_ENV =	CC="${CC}" CFLAGS="${CFLAGS}"

do-build:
	cd ${WRKSRC} && ./Gmake

.include <bsd.port.mk>
