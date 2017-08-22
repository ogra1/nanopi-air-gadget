
[![Snap Status](https://build.snapcraft.io/badge/ogra1/nanopi-air-gadget.svg)](https://build.snapcraft.io/user/ogra1/nanopi-air-gadget)

# NanoPi NEO Air Gadget Snap

This repository contains the source for an Ubuntu Core gadget snap
for the NanoPi NEO Air. Building it with snapcraft will
automatically pull, configure, patch and build the git.denx.de/u-boot.git
upstream source for `nanopi_neo_defconfig` at release `v2017.05` and produce
a bootable gadget snap with the resulting binaries.

## Gadget Snaps

Gadget snaps are a special type of snaps that contain device specific support
code and data. You can read more about them in the snapd wiki
https://github.com/snapcore/snapd/wiki/Gadget-snap

## Building

*NOTE: this gadget snap can only build under 17.10 (artful) or with a gcc6 cross
compiler, the sunxi u-boot build has a hard requirement on gcc6!*

### Natively on armhf

Create an artful (17.10) chroot, install snapcraft and git inside it, chroot into it
and clone this tree.

To build the gadget snap locally on a native armhf system just run `snapcraft`
in the toplevel of the tree.

### Cross on x86 systems

Just run `snapcraft` in the toplevel of the tree, snapcraft will pull the linaro gcc6
cross compiler into the build environment as needed.

```
snapcraft
```

