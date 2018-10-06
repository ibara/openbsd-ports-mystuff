# $OpenBSD: Makefile.template,v 1.78 2018/07/09 15:00:06 jca Exp $

COMMENT =	QuakeWorld server
DISTNAME =	mvdsv-0.32

GH_ACCOUNT =	deurk
GH_PROJECT =	mvdsv
GH_COMMIT =	873484474f6e0bdbecd0bcc6a6bac984e7ea2428

CATEGORIES =	games

MAINTAINER =	Tom Murphy <openbsd@pertho.net>

# GPLv2+
PERMIT_PACKAGE_CDROM =	Yes

WANTLIB += c curl m pthread

LIB_DEPENDS =	net/curl

CONFIGURE_STYLE =	simple

MAKE_FLAGS =	CC="${CC}" CFLAGS="${CFLAGS} -I${LOCALBASE}/include" \
		LDFLAGS="${LDFLAGS} -L${LOCALBASE}/lib -lcurl -lm"

NO_TEST =	Yes

WRKSRC =	${WRKDIST}/build/make

SAMPLES_DIR =	${PREFIX}/share/examples/mvdsv

# No upstream install target.
do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/mvdsv ${PREFIX}/bin
	${INSTALL_DATA_DIR} ${SAMPLES_DIR}
	${INSTALL_DATA} ${FILESDIR}/qwprogs.dat ${SAMPLES_DIR}
	${INSTALL_DATA} ${FILESDIR}/server.cfg ${SAMPLES_DIR}

.include <bsd.port.mk>
