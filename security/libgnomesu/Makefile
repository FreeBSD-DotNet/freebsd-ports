# Created by: Adam Weinberger <adamw@FreeBSD.org>
# $FreeBSD$
#    $MCom: ports/security/libgnomesu/Makefile,v 1.2 2007/05/19 21:36:21 marcus Exp $

PORTNAME=	libgnomesu
PORTVERSION=	1.0.0
PORTREVISION=	12
CATEGORIES=	security gnome
MASTER_SITES=	http://members.chello.nl/~h.lai/libgnomesu/

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Library and frontend for running commands as root

USES=		gmake gettext-tools libtool pathfix pkgconfig
GNU_CONFIGURE=	yes
USE_GNOME=	gnomeprefix libgnomeui
CONFIGURE_ARGS+=--disable-install-pam \
		--disable-setuid-error
CPPFLAGS+=	-I${LOCALBASE}/include
LIBS+=		-L${LOCALBASE}/lib
INSTALL_TARGET=	install-strip

SUB_FILES=	pkg-message

OPTIONS_DEFINE=	DOCS EXAMPLES

post-patch:
	@${REINPLACE_CMD} -e 's|-DGTK_DISABLE_DEPRECATED||g' \
		${WRKSRC}/src/Makefile.in

post-install:
	@${MKDIR} ${STAGEDIR}${EXAMPLESDIR}
	${INSTALL_DATA} ${FILESDIR}/gnomesu-pam.sample ${STAGEDIR}${EXAMPLESDIR}
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${WRKSRC}/doc/api.html ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${WRKSRC}/doc/libgnomesu.css ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
