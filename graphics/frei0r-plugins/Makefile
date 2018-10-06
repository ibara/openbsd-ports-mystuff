# $OpenBSD$

COMMENT =	minimalistic plugin API for video effects
CATEGORIES =	graphics multimedia

DISTNAME =	frei0r-plugins-1.6.1
MASTER_SITES =	https://files.dyne.org/frei0r/releases/

HOMEPAGE =	https://frei0r.dyne.org/
MAINTAINER =	Raphael Graf <r@undefined.ch>

# GPLv2+
PERMIT_PACKAGE_CDROM = Yes

WANTLIB =	${COMPILER_LIBCXX} m cairo

LIB_DEPENDS =	graphics/cairo

MODULES =	devel/cmake

CONFIGURE_ARGS = -DWITHOUT_OPENCV:BOOL=ON

NO_TEST =	Yes

.include <bsd.port.mk>
