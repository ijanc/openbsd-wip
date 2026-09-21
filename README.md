# openbsd-wip

OpenBSD work in progress ports.

Ports here are being worked on before submission to ports@ and may not
always build. Each port directory is complete (Makefile, distinfo, pkg/,
patches/). A TODO file in a port lists what is missing before it can be
sent; an UPDATE file explains an update to an in-tree port. Ports are
removed once committed upstream.

## Usage

Clone into `/usr/ports` and add it to `PORTSDIR_PATH` in `/etc/mk.conf`:

    PORTSDIR_PATH=${PORTSDIR}:${PORTSDIR}/openbsd-wip

Ports in `/usr/ports` take precedence over the ones here.

## Repositories

- https://git.sr.ht/~ijanc/openbsd-wip
- https://github.com/ijanc/openbsd-wip
