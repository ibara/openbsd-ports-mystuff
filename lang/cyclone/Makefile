# $OpenBSD$

COMMENT =	R7RS Scheme to C compiler
DISTNAME =	cyclone-0.9.1
CATEGORIES =	lang

HOMEPAGE =	https://justinethier.github.io/cyclone/
MAINTAINER =	Brian Callahan <bcallah@openbsd.org>

# MIT
PERMIT_PACKAGE_CDROM =	Yes

WANTLIB += c ck m pthread

MASTER_SITES =	https://mirrors.nycbug.org/pub/distfiles/

BUILD_DEPENDS =	math/libtommath

LIB_DEPENDS =	devel/ck

RUN_DEPENDS =	math/libtommath

# COMP_CFLAGS is what cyclone calls cc with.
# LIBS is what cyclone calls cc with when linking.
USE_GMAKE =	Yes
MAKE_FLAGS =	CFLAGS="${CFLAGS} -fPIC -I${LOCALBASE}/include -Iinclude" \
		COMP_CFLAGS="${CFLAGS} -fPIC -I${LOCALBASE}/include" \
		LDFLAGS="${LDFLAGS} -L${LOCALBASE}/lib -L." \
		LIBS="${LDFLAGS} -L${LOCALBASE}/lib -pthread -lcyclone -lck -lm -ltommath"

FAKE_FLAGS =	DESTDIR=""

# Needs to be installed to run the tests...
TEST_DEPENDS =	${BASE_PKGPATH}

.include <bsd.port.mk>
