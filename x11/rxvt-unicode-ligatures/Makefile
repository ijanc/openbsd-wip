COMMENT=	unicode rxvt clone with harfbuzz ligatures and 24-bit colour

V=		9.31
DISTNAME=	rxvt-unicode-${V}
PKGNAME=	rxvt-unicode-ligatures-${V}
EXTRACT_SUFX=	.tar.bz2

CATEGORIES=	x11

FIX_EXTRACT_PERMISSIONS=	Yes

SITES=		http://dist.schmorp.de/rxvt-unicode/ \
		http://dist.schmorp.de/rxvt-unicode/Attic/

HOMEPAGE=	http://software.schmorp.de/pkg/rxvt-unicode.html

MAINTAINER=	Murilo Ijanc <murilo@ijanc.org>

# GPLv3+
PERMIT_PACKAGE=	Yes

WANTLIB += ${COMPILER_LIBCXX} X11 Xext Xft Xmu Xrender Xt c fontconfig
WANTLIB += freetype harfbuzz m perl ptytty

COMPILER=	base-clang ports-gcc
DEBUG_PACKAGES=	${BUILD_PACKAGES}

CONFIGURE_STYLE=  autoconf
AUTOCONF_VERSION= 2.71

LIB_DEPENDS=	devel/harfbuzz \
		sysutils/libptytty

CONFIGURE_ARGS=	--enable-unicode3 \
		--enable-256-color \
		--enable-24-bit-color \
		--enable-wide-glyphs \
		--enable-harfbuzz \
		--disable-fallback \
		--disable-pixbuf \
		--disable-startup-notification \
		--disable-fading \
		--disable-rxvt-scroll \
		--disable-next-scroll \
		--disable-xterm-scroll \
		--disable-iso14755 \
		--disable-keepscrolling \
		--disable-slipwheeling \
		--disable-smart-resize

FAKE_FLAGS=	INSTALL_DATA="${INSTALL_DATA}" \
		INSTALL_PROGRAM="${INSTALL_PROGRAM}"

MAKE_ENV+=	TERMINFO=${WRKINST}${PREFIX}/share/terminfo

CONFIGURE_ENV+=	CPPFLAGS="-I${X11BASE}/include" \
		pt_cv_tty_group=yes

post-patch:
	rm ${WRKSRC}/src/perl/matcher${PATCHORIG}

.include <bsd.port.mk>
