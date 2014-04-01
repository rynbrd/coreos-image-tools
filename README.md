CoreOS Image Tools
==================
A set of tools for manipulating CoreOS images.

coreos-mount
------------
Mount/Unmount partitions in an image. To mount the root partition at
/mnt/coreos:

    $ coreos-mount mount coreos.bin ROOT-A /mnt/coreos

To unmount the partition:

	$ coreos-mount umount coreos.bin ROOT-A

Common labels are:

- EFI-SYSTEM
- ROOT-A
- ROOT-B
- OEM
- STATE

See the CoreOS docs for additional partition details.

coreos-rw
---------
Enable/Disable write mode on a CoreOS root partition. To enable write mode on
the image attached to loop0:

    $ coreos-rw enable /dev/mapper/loop0p3

To disable write mode:

    $ coreos-rw disable /dev/mapper/loop0p3

License
-------
This software project is licensed under the BSD-derived license and is
copyright (c) 2014 Ryan Bourgeois. A copy of the license is included in the
LICENSE file. If it is missing then a copy may be found on the project page.
