# $FreeBSD$

PORTNAME=		kproperty
DISTVERSION=		3.1.0
CATEGORIES=		x11-toolkits kde
MASTER_SITES=		KDE/stable/${PORTNAME}/src
DIST_SUBDIR=		KDE/${PORTNAME}

MAINTAINER=		kde@FreeBSD.org
COMMENT=		Property editing framwork

USES=			cmake:outsource gettext kde:5 qt:5 tar:xz
USE_KDE=		ecm config coreaddons guiaddons i18n widgetsaddons
USE_QT=			core gui widgets xml \
			buildtools_build qmake_build qml

CONFLICTS_INSTALL=	calligra-2*

.include <bsd.port.mk>
