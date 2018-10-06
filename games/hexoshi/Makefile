# $OpenBSD$

V =		0.2
COMMENT =	free Metroidvania game
DISTNAME =	hexoshi-${V}-src
PKGNAME =	hexoshi-${V}
CATEGORIES =	games x11

HOMEPAGE =	http://hexoshi.nongnu.org/
MAINTAINER =	Brian Callahan <bcallah@openbsd.org>

# GPLv3+
PERMIT_PACKAGE_CDROM =	Yes

#WANTLIB +=	c curses iconv intl

MASTER_SITES =	${MASTER_SITE_SAVANNAH:=hexoshi/${V}/}

MODULES =	lang/python
MODPY_VERSION =	${MODPY_DEFAULT_VERSION_3}

.include <bsd.port.mk>
