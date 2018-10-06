# $OpenBSD$

COMMENT =	C and C++ program reducer
DISTNAME =	${GH_PROJECT}-2.8.0.20180824
CATEGORIES =	devel

# Switch to GH_TAGNAME once 2.9.0 is out
GH_ACCOUNT =	csmith-project
GH_PROJECT =	creduce
#GH_TAGNAME =	${GH_PROJECT}-2.9.0
GH_COMMIT =	921324f8c7eec1ec94f329e4e3e7a492dee90b2f

HOMEPAGE =	https://embed.cs.utah.edu/creduce/
MAINTAINER =	Brian Callahan <bcallah@openbsd.org>

# BSD
PERMIT_PACKAGE_CDROM =	Yes

# This links libLLVM-6.0.so
WANTLIB += ${COMPILER_LIBCXX} c m

MODULES =	devel/cmake

BUILD_DEPENDS =	${RUN_DEPENDS}

# XXX: devel/llvm should really be a LIB_DEPENDS
# Revisit if libLLVM.so is ever versioned
RUN_DEPENDS =	devel/llvm>=6.0,<6.1 \
		devel/p5-Exporter-Lite \
		devel/p5-Getopt-Tabular \
		sysutils/p5-File-Which \
		textproc/p5-Regexp-Common

NO_TEST =	Yes

.include <bsd.port.mk>
