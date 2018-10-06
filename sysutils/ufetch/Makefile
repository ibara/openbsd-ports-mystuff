# $OpenBSD$

COMMENT =	tiny system info for Unix-like operating systems

DISTNAME =	ufetch-2018.09.08
CATEGORIES =	sysutils

HOMEPAGE =	https://gitlab.com/jschx/ufetch/

# ISC
PERMIT_PACKAGE_CDROM =	Yes

MASTER_SITES =	https://notabug.org/jasval/ufetch-releases/raw/master/

NO_BUILD =	Yes
NO_TEST =	Yes

PKG_ARCH =	*

do-install:
	${INSTALL_SCRIPT} ${WRKSRC}/ufetch-openbsd ${PREFIX}/bin/ufetch
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/ufetch/
	${INSTALL_DATA} ${WRKSRC}/LICENSE ${PREFIX}/share/doc/ufetch/LICENSE

.include <bsd.port.mk>
