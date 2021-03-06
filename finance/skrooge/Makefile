# $FreeBSD$

PORTNAME=	skrooge
PORTVERSION=	1.12.5
PORTREVISION=	1
CATEGORIES=	finance kde
MASTER_SITES=	KDE/stable/${PORTNAME}

MAINTAINER=	kde@FreeBSD.org
COMMENT=	KDE4 personal finance manager

PORTSCOUT=	limit:^1\.

BUILD_DEPENDS=	xsltproc:textproc/libxslt
LIB_DEPENDS=	libofx.so:finance/libofx \
		libqca.so:devel/qca \
		libkactivities.so:x11/kactivities

USES=		cmake:outsource gettext grantlee:4 kde:4 shared-mime-info \
		sqlite:3 tar:xz
USE_QT4=	qmake_build moc_build uic_build rcc_build designer_build \
		corelib dbus gui script sql webkit xml sql-sqlite3_run
USE_KDE=	automoc4 kdelibs pimlibs
USE_LDCONFIG=	yes

PLIST_SUB=	VERSION=${PORTVERSION}

# Skrooge creates several empty directories due to how it calls CMake's
# install(DIRECTORY ...) function, so we need some code to remove them.
post-install:
	${FIND} ${STAGEDIR}${PREFIX}/share/apps/skrooge/html \
		-type d -empty -delete

.include <bsd.port.mk>
