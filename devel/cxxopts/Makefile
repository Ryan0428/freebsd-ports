# $FreeBSD$

PORTNAME=	cxxopts
DISTVERSIONPREFIX=	v
DISTVERSION=	2.1.1
CATEGORIES=	devel

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Lightweight C++ command line option parser

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

USES=		cmake:outsource
USE_GITHUB=	yes
GH_ACCOUNT=	jarro2783
NO_ARCH=	yes

PLIST_FILES=	include/cxxopts.hpp \
		lib/cmake/cxxopts/cxxopts-config-version.cmake \
		lib/cmake/cxxopts/cxxopts-config.cmake \
		lib/cmake/cxxopts/cxxopts-targets.cmake

.include <bsd.port.mk>
