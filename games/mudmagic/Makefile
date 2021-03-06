# Created by: trasz <trasz@pin.if.uz.zgora.pl>
# $FreeBSD$

PORTNAME=	mudmagic
PORTVERSION=	1.9
PORTREVISION=	18
CATEGORIES=	games
MASTER_SITES=	http://www.mudmagic.com/mud-client/downloads/

MAINTAINER=	ports@FreeBSD.org
COMMENT=	GTK+ based MUD client

LICENSE=	GPLv2+
LICENSE_FILE=	${WRKSRC}/COPYING

BROKEN=		Does not build with recent devel/glib20

LIB_DEPENDS=	libcurl.so:ftp/curl \
		libpcre.so:devel/pcre \
		libpng.so:graphics/png \
		libexpat.so:textproc/expat2 \
		libfreetype.so:print/freetype2 \
		libfontconfig.so:x11-fonts/fontconfig

USES=		gettext-runtime gmake libtool localbase pathfix \
		pkgconfig python:2.7 sqlite
USE_GNOME=	cairo gdkpixbuf2 gtk20 libglade2 libxml2
GNU_CONFIGURE=	yes
INSTALL_TARGET=	install-strip
USE_LDCONFIG=	yes
LIBS+=		`${PYTHON_CMD:T}-config --libs` `pkg-config --libs gtk+-x11-2.0` `pkg-config --libs libcurl`

post-patch:
	@${REINPLACE_CMD} -e 's|glib/.*\.h>|glib.h>|g' \
		${WRKSRC}/src/network/network.h \
		${WRKSRC}/src/configuration/configuration.h \
		${WRKSRC}/src/interface/tools.c \
		${WRKSRC}/src/interface/theme_select.c \
		${WRKSRC}/src/protocols/http.h \
		${WRKSRC}/src/utils/gamelist.c \
		${WRKSRC}/src/utils/muderr.h \
		${WRKSRC}/src/utils/alias_triggers.c \
		${WRKSRC}/src/utils/gamelist.h

.include <bsd.port.mk>
