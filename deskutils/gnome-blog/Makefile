# Created by: Adam Weinberger <adamw@FreeBSD.org>
# $FreeBSD$
#   $MCom: ports/deskutils/gnome-blog/Makefile,v 1.5 2007/08/08 21:52:36 mezz Exp $

PORTNAME=	gnome-blog
PORTVERSION=	0.9.1
PORTREVISION=	7
CATEGORIES=	deskutils gnome
MASTER_SITES=	GNOME
DIST_SUBDIR=	gnome2

MAINTAINER=	gnome@FreeBSD.org
COMMENT=	GNOME app to post to blogs

USES=		gettext gmake pathfix pkgconfig python tar:bzip2
GNU_CONFIGURE=	yes
USE_GNOME=	gnomeprefix pygnome2 intlhack
CPPFLAGS+=	-I${LOCALBASE}/include
LDFLAGS+=	-L${LOCALBASE}/lib

GCONF_SCHEMAS=	gnomeblog.schemas

.include <bsd.port.mk>
