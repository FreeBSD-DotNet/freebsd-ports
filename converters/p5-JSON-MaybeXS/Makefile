# Created by: Sunpoet Po-Chuan Hsieh <sunpoet@FreeBSD.org>
# $FreeBSD$

PORTNAME=	JSON-MaybeXS
PORTVERSION=	1.003005
CATEGORIES=	converters perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	Use Cpanel::JSON::XS with a fallback to JSON::PP

LICENSE=	ART10 GPLv1
LICENSE_COMB=	dual

BUILD_DEPENDS=	p5-Cpanel-JSON-XS>=2.3310:converters/p5-Cpanel-JSON-XS
RUN_DEPENDS:=	${BUILD_DEPENDS}
TEST_DEPENDS=	p5-JSON-XS>=0:converters/p5-JSON-XS \
		p5-Test-Without-Module>=0.17:devel/p5-Test-Without-Module

USE_PERL5=	configure
USES=		perl5

.include <bsd.port.mk>
