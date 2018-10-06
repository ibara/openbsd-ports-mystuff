# $OpenBSD$

MODPY_EGG_VERSION =	1.0.5
COMMENT =	encrypted Content Encoding for HTTP
DISTNAME =	http_ece-${MODPY_EGG_VERSION}
PKGNAME =	py-http_ece-${MODPY_EGG_VERSION}
CATEGORIES =	www

HOMEPAGE =	https://github.com/martinthomson/encrypted-content-encoding
MAINTAINER =	Pamela Mosiejczuk <pamela@cranky.work>

# MIT
PERMIT_PACKAGE_CDROM =	Yes

MODULES =	lang/python
MODPY_SETUPTOOLS =	Yes
MODPY_PI =	Yes

FLAVORS =	python3
FLAVOR ?=

RUN_DEPENDS =	security/py-cryptography${MODPY_FLAVOR}

# Only use with FLAVOR=python3! No python2 version of flake8.
# It doesn't run/have any tests anyway...
TEST_DEPENDS =	${RUN_DEPENDS} \
		devel/flake8 \
		devel/py-nose${MODPY_FLAVOR} \
		devel/py-mock${MODPY_FLAVOR} \
		devel/py-coverage${MODPY_FLAVOR}

.include <bsd.port.mk>
