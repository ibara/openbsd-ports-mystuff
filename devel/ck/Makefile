# $OpenBSD$

# So says the configure script
ONLY_FOR_ARCHS =	aarch64 amd64 arm i386 powerpc sparc64

COMMENT =	library for high performance concurrent systems
DISTNAME =	ck-0.6.0
CATEGORIES =	devel

SHARED_LIBS +=	ck                        0.0 # 0.6.0

HOMEPAGE =	http://concurrencykit.org/
MAINTAINER =	Brian Callahan <bcallah@openbsd.org>

# BSD
PERMIT_PACKAGE_CDROM =	Yes

MASTER_SITES =	http://concurrencykit.org/releases/

CONFIGURE_STYLE =	simple
CONFIGURE_ARGS =	--mandir="${PREFIX}/man"
CONFIGURE_ENV =		LIBck_VERSION="${LIBck_VERSION}"

MAKE_ENV =	LIBck_VERSION="${LIBck_VERSION}"

NO_TEST =	Yes

.include <bsd.port.mk>
