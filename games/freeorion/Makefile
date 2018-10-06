# $OpenBSD$

V =		0.4.8
COMMENT =	turn-based space empire and galactic conquest computer game
DISTNAME =	FreeOrion_v${V}_2018-08-23.26f16b0_Source
PKGNAME =	freeorion-${V}
CATEGORIES =	games

HOMEPAGE =	https://www.freeorion.org/
MAINTAINER =	Tom Murphy <openbsd@pertho.net>

# Game: GPLv2+
# Assets: CC-BY-SA 3.0
PERMIT_PACKAGE_CDROM =	Yes

WANTLIB += ${COMPILER_LIBCXX} GL GLEW GLU SDL2 boost_atomic-mt
WANTLIB += boost_chrono-mt boost_date_time-mt boost_filesystem-mt
WANTLIB += boost_iostreams-mt boost_locale-mt boost_log-mt boost_log_setup-mt
WANTLIB += boost_python-mt boost_regex-mt boost_serialization-mt
WANTLIB += boost_signals-mt boost_system-mt boost_thread-mt c
WANTLIB += freetype m ogg openal png python2.7 vorbis vorbisenc
WANTLIB += vorbisfile z

MASTER_SITES =	https://github.com/freeorion/freeorion/releases/download/v${V}/

MODULES =	devel/cmake \
		lang/python

BUILD_DEPENDS =	devel/cppcheck \
		devel/py-codestyle

LIB_DEPENDS =	audio/libogg \
		audio/libvorbis \
		audio/openal \
		devel/sdl2 \
		devel/boost \
		graphics/glew \
		graphics/png

RUN_DEPENDS =	devel/desktop-file-utils \
		x11/gtk+3,-guic

NO_TEST =	Yes

WRKSRC =	${WRKDIR}/src-tarball

post-install:
	${MODPY_BIN} ${MODPY_LIBDIR}/compileall.py \
	${PREFIX}/share/freeorion/default

.include <bsd.port.mk>
