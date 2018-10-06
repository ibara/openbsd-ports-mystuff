# $OpenBSD: Makefile.template,v 1.78 2018/07/09 15:00:06 jca Exp $

V =		246.00
COMMENT =	manage modifications for Infinity Engine games
DISTNAME =	weidu-v${V}
PKGNAME =	weidu-${V}
CATEGORIES =	games

HOMEPAGE =	https://www.weidu.org
MAINTAINER =	Thomas Frohwein <thfr@openbsd.org>

# GPLv2 (weidu), 3-clause BSD (elkhound)
PERMIT_PACKAGE_CDROM =	Yes

WANTLIB += c m

MASTER_SITES =	https://thfr.info/distfiles/
EXTRACT_SUFX =	.tar.xz

BUILD_DEPENDS =	devel/bison \
		lang/ocaml

USE_GMAKE =	Yes
ALL_TARGET =	weidu weinstall tolower
MAKE_FLAGS =	V=1
MAKE_ENV =	CC=${CC}

NO_TEST =	Yes

#SUBST_VARS +=	CFLAGS

# examples directory is used during build; no easy way to sidestep it and the
# hardcoded g++ in the examples
post-patch:
	sed -i "s,g++,${CXX},g" \
		${WRKSRC}/elkhound-src-2018-05-12/elkhound/examples/*/*
	${SUBST_CMD} ${WRKSRC}/elkhound-src-2018-05-12/smbase/sm_config.pm
	${SUBST_CMD} ${WRKSRC}/elkhound-src-2018-05-12/elkhound/Makefile.in
	${SUBST_CMD} ${WRKSRC}/elkhound-src-2018-05-12/elkhound/c/Makefile.in
	${SUBST_CMD} ${WRKSRC}/elkhound-src-2018-05-12/elkhound/perftest/test-ver
	${SUBST_CMD} ${WRKSRC}/elkhound-src-2018-05-12/smbase/Makefile.in
	cp ${WRKSRC}/sample.Configuration ${WRKSRC}/Configuration

do-configure:
	cd ${WRKSRC}/elkhound-src-2018-05-12/ast && ./configure
	cd ${WRKSRC}/elkhound-src-2018-05-12/elkhound && ./configure
	cd ${WRKSRC}/elkhound-src-2018-05-12/smbase && ./configure -no-dash-g

# build elkhound first, then use it to build weidu
do-build:
	cd ${WRKSRC}/elkhound-src-2018-05-12 && \
		env -i ${MAKE_ENV} ${MAKE_PROGRAM} ${MAKE_FLAGS} \
		-f ${MAKE_FILE} all
	cd ${WRKSRC} && \
		env -i ${MAKE_ENV} ${MAKE_PROGRAM} ${MAKE_FLAGS} \
		-f ${MAKE_FILE} ${ALL_TARGET}

do-install:
	${INSTALL_PROGRAM} ${WRKBUILD}/tolower.asm.exe ${PREFIX}/bin/tolower
	${INSTALL_PROGRAM} ${WRKBUILD}/weidu.asm.exe ${PREFIX}/bin/weidu
	${INSTALL_PROGRAM} ${WRKBUILD}/weinstall.asm.exe ${PREFIX}/bin/weinstall

.include <bsd.port.mk>
