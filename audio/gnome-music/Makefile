# Created by: Gustau Perez <gustau.perez@gmail.com>
# $FreeBSD$

PORTNAME=	gnome-music
PORTVERSION=	3.18.2
PORTREVISION=	2
CATEGORIES=	audio gnome
MASTER_SITES=	GNOME
DIST_SUBDIR=	gnome3

MAINTAINER=	gnome@FreeBSD.org
COMMENT=	GNOME music playing application

BUILD_DEPENDS=	itstool:textproc/itstool
LIB_DEPENDS=	libgrilo-0.2.so:net/grilo2 \
		libmediaart-2.0.so:multimedia/libmediaart

PORTSCOUT=	limitw:1,even

USES=		gettext gmake gnome libtool pathfix pkgconfig python:3 tar:xz
USE_LDCONFIG=	yes
USE_GNOME=	gnomedesktop3 gtk30 intltool introspection:build
GNU_CONFIGURE=	yes
USE_GSTREAMER1=	ogg mpg123
INSTALLS_ICONS=	yes
CPPFLAGS+=	-I${LOCALBASE}/include
LDFLAGS+=	-L${LOCALBASE}/lib
MAKE_ENV=	XDG_CACHE_HOME=${WRKDIR}
INSTALL_TARGET=	install-strip

GLIB_SCHEMAS=	org.gnome.Music.gschema.xml

.include <bsd.port.mk>
