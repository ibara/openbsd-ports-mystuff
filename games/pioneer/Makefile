# $OpenBSD: Makefile.template,v 1.71 2014/07/10 12:33:17 sthen Exp $

COMMENT =		game of lonely space and adventure

CATEGORIES =		games

HOMEPAGE =		https://pioneerspacesim.net/

# GPLv3 only
PERMIT_PACKAGE_CDROM =	Yes

WANTLIB += ${COMPILER_LIBCXX}
WANTLIB += GL SDL2 SDL2_image assimp c freetype m png pthread
WANTLIB += sigc-2.0 vorbisfile z

GH_ACCOUNT =		pioneerspacesim
GH_PROJECT =		pioneer
GH_TAGNAME =		20180203

COMPILER =		base-clang ports-gcc
BUILD_DEPENDS =		${MODGNU_AUTOCONF_DEPENDS} \
			${MODGNU_AUTOMAKE_DEPENDS}
LIB_DEPENDS =		audio/libvorbis \
			devel/libsigc++-2 \
			devel/sdl2-image \
			multimedia/assimp

USE_GMAKE =		Yes
CONFIGURE_STYLE =	gnu
CONFIGURE_ENV =		CPPFLAGS="-I${LOCALBASE}/include -I${X11BASE}/include" \
			LDFLAGS="-L${LOCALBASE}/lib -L${X11BASE}/lib" \
			PIONEER_DATA_DIR=${PREFIX}/share/pioneer/

MAKE_FLAGS =		V=1

AUTOCONF_VERSION =	2.69
AUTOMAKE_VERSION =	1.15

pre-configure:
	cd ${WRKSRC} && env \
		AUTOCONF_VERSION=${AUTOCONF_VERSION} \
		AUTOMAKE_VERSION=${AUTOMAKE_VERSION} \
		sh bootstrap

.include <bsd.port.mk>
