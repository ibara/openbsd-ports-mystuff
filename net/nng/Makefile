# $OpenBSD$

COMMENT =               nanomsg-next-generation -- light-weight brokerless messaging

CATEGORIES =            net

GH_ACCOUNT =            opunix
GH_PROJECT =            nng
GH_TAGNAME =            9683efb2adee597304151299e5f55e6ab693605a
MASTER_SITES =          https://github.com/nanomsg/${GH_PROJECT}/archive/
DISTFILES =             ${GH_TAGNAME}.zip

HOMEPAGE =              https://nanomsg.github.io/nng/
MAINTAINER =            opunix <francisc.simon@evalgo.org>

PERMIT_PACKAGE_CDROM =  Yes

SHARED_LIBS +=          nng             0.0 # 1.0

BUILD_DEPENDS =         devel/cmake \
                        devel/ninja \
                        archivers/unzip

WANTLIB +=              c pthread

SEPARATE_BUILD =        Yes
CONFIGURE_ARGS =        -G Ninja

MODULES +=              devel/cmake

.include <bsd.port.mk>
