# $OpenBSD$

COMMENT =	marble game inspired by Marble Madness
CATEGORIES =	games x11

GH_ACCOUNT =	trackballs
GH_PROJECT =	trackballs
GH_TAGNAME =	v1.3.1

HOMEPAGE =	https://trackballs.github.io/

# source GPLv2+
# music GPLv2+ or Ethymos Free Music Licence
PERMIT_PACKAGE_CDROM =	Yes

#WANTLIB += GL GLU SDL SDL_image SDL_mixer SDL_ttf c gmp guile

MODULES =	devel/cmake

BUILD_DEPENDS =	devel/gettext-tools

LIB_DEPENDS =	devel/gmp \
		devel/sdl2-image \
		devel/sdl2-mixer \
		devel/sdl2-ttf \
		lang/guile2

RUN_DEPENDS =	devel/desktop-file-utils \
		x11/gtk+3,-guic

.include <bsd.port.mk>
