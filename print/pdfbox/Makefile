# Created by: Pedro Giffuni
# $FreeBSD$

PORTNAME=	pdfbox
PORTVERSION=	2.0.11
CATEGORIES=	print textproc java
MASTER_SITES=	APACHE/pdfbox/${PORTVERSION}
DISTFILES=	${JAR_NAMES:S/$/-${PORTVERSION}.jar/}
EXTRACT_ONLY=	# none

MAINTAINER=	ale@FreeBSD.org
COMMENT=	Java tool for working with PDF documents

LICENSE=	APACHE20

RUN_DEPENDS=	${JAVALIBDIR}/bcmail.jar:java/bouncycastle15 \
		${JAVALIBDIR}/commons-logging.jar:java/jakarta-commons-logging \
		${JAVALIBDIR}/commons-io.jar:devel/jakarta-commons-io

JAR_NAMES=	pdfbox fontbox preflight xmpbox pdfbox-tools pdfbox-debugger

USE_JAVA=	yes
NO_BUILD=	yes
NO_ARCH=		yes

PLIST_FILES=	${JAR_NAMES:S/^/%%JAVAJARDIR%%\//:S/$/.jar/}

do-install:
	@${ECHO_MSG} -n ">> Installing JAR files in ${JAVAJARDIR}..."
	@${MKDIR} ${STAGEDIR}${JAVAJARDIR}
.for f in ${JAR_NAMES}
	${INSTALL_DATA} ${DISTDIR}/${f}-${PORTVERSION}.jar \
		${STAGEDIR}${JAVAJARDIR}/${f}.jar
.endfor
	@${ECHO_MSG} " [ DONE ]"

.include <bsd.port.mk>
