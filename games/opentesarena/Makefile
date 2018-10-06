# $OpenBSD$

V =		0.7.0
COMMENT =	open-source re-implementation of The Elder Scrolls: Arena
PKGNAME =	opentesarena-${V}
CATEGORIES =	games x11

GH_ACCOUNT =	afritz1
GH_PROJECT =	OpenTESArena
GH_TAGNAME =	opentesarena-${V}

MAINTAINER =	Brian Callahan <bcallah@openbsd.org>

# MIT
PERMIT_PACKAGE_CDROM =	Yes

WANTLIB += ${COMPILER_LIBCXX} SDL2 WildMidi c m openal

# C++11
COMPILER =	base-clang ports-gcc ports-clang

MODULES =	devel/cmake

LIB_DEPENDS =	audio/openal \
		audio/wildmidi \
		devel/sdl2

NO_TEST =	Yes

# No upstream install routine
do-install:
	${INSTALL_PROGRAM} ${WRKBUILD}/TESArena ${PREFIX}/bin

.include <bsd.port.mk>
