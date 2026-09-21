COMMENT =	keyboard-select and resize-font perl extensions for urxvt

V =		2.3
RF_COMMIT =	b5935806f159594f516da9b4c88bf1f3e5225cfd
DIST_TUPLE =	github muennich urxvt-perls ${V} .
DIST_TUPLE +=	github simmel urxvt-resize-font ${RF_COMMIT} resize-font

CATEGORIES =	x11

MAINTAINER =	Murilo Ijanc <murilo@ijanc.org>

# GPLv2 (keyboard-select), ISC (resize-font)
PERMIT_PACKAGE =	Yes

RUN_DEPENDS =	rxvt-unicode-*|rxvt-unicode-ligatures-*:x11/rxvt-unicode

NO_BUILD =	Yes
NO_TEST =	Yes
PKG_ARCH =	*

EXTDIR =	${PREFIX}/lib/urxvt/perl

do-install:
	${INSTALL_DATA_DIR} ${EXTDIR}
	${INSTALL_DATA} ${WRKSRC}/keyboard-select ${EXTDIR}
	${INSTALL_DATA} ${WRKSRC}/resize-font/resize-font ${EXTDIR}

.include <bsd.port.mk>
