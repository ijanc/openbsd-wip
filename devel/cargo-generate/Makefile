# aws-lc-sys has constants in .text
# https://github.com/awslabs/s2n-bignum/pull/242
.if ${MACHINE_ARCH} == "amd64" || ${MACHINE_ARCH} == "aarch64"
USE_NOEXECONLY =	Yes
.endif

# ring-v0.17 does not support this arch
NOT_FOR_ARCHS =		sparc64

COMMENT =		generate Rust projects from template repositories

GH_ACCOUNT =		cargo-generate
GH_PROJECT =		cargo-generate
GH_TAGNAME =		v0.25.0

CATEGORIES =		devel

MAINTAINER =		Murilo Ijanc <murilo@ijanc.org>

# MIT/Apache 2.0
PERMIT_PACKAGE =	Yes

# C11
COMPILER =		base-clang ports-gcc
COMPILER_LANGS =	c

WANTLIB +=		${MODCARGO_WANTLIB} m

MODULES =		devel/cargo

CONFIGURE_STYLE =	cargo

SEPARATE_BUILD =	Yes

.include "crates.inc"
.include <bsd.port.mk>
