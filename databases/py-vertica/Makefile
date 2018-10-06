# $OpenBSD$

MODPY_EGG_VERSION =	0.7.4
COMMENT =	Python interface to the Vertica database system
PKGNAME =	py-${DISTNAME}

GH_ACCOUNT =	vertica
GH_PROJECT =	vertica-python
GH_TAGNAME =	${MODPY_EGG_VERSION}

CATEGORIES =	databases

# MIT
PERMIT_PACKAGE_CDROM =	Yes

FLAVORS =      	python3
FLAVOR ?=

MODULES =	lang/python
MODPY_SETUPTOOLS = 	Yes

RUN_DEPENDS =	devel/py-dateutil${MODPY_FLAVOR} \
		devel/py-tz${MODPY_FLAVOR}

TEST_DEPENDS =	${RUN_DEPENDS} \
		devel/py-future${MODPY_FLAVOR}

.include <bsd.port.mk>
