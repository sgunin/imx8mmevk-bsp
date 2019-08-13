# NXP i.MX 8M mini EVK Manifest repo
This repo is used to download manifests for i.MX BSP releases for NXP i.MX 8M mini EVK board.

Specific instructions will reside in READMEs in each branch.

Original repo avialable via link - https://source.codeaurora.org/external/imx/imx-manifest/tree/?h=imx-linux-sumo.

This manual describes how to deploy the image build environment under Ubuntu 16.04.5.

Install necessary packages:

`$: sudo apt install build-essential git-core libncurses5-dev flex bison texinfo zip unzip zlib1g-dev gettext u-boot-tools g++ xz-utils mtd-utils gawk diffstat gcc-multilib lzop bc chrpath`

To get the BSP you need to have `repo` installed and use it as:

Install the `repo` utility:

`$: apt install repo`

Download the BSP source:
`
$: mkdir imx8mmevk
$: cd imx8mmevk
$: repo init -u https://github.com/sgunin/imx8mmevk.git -b <branch>
$: repo sync
`
where <branch> is Yocto branch name (thud, sumo etc).

Yocto manual avialable via link https://www.yoctoproject.org/docs/?section=developer-manuals

At the end of the commands you have every metadata you need to start work with.
