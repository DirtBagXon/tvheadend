Tvheadend
========================================
(c) 2006 - 2020 Tvheadend Foundation CIC

Repo
----

This is an unofficial repo that holds the stable release of TVHeadend 4.2.8 \
plus minimal stable fixes, and a few backported features, to keep it functional \
while development appears to have stalled in the official repo.

Use at your own risk.

What it is
----------

Tvheadend is a TV streaming server and digital video recorder.

It supports the following inputs:

  * DVB-C(2)
  * DVB-T(2)
  * DVB-S(2)
  * ATSC
  * SAT>IP
  * HDHomeRun
  * IPTV
    * UDP
    * HTTP

It supports the following outputs:

  * HTTP
  * HTSP (own protocol)
  * SAT>IP

How to build for Linux
----------------------

First you need to configure:

	$ git tag -a v4.2.8.1-dirtbagxon -m "4.2.8.1-dirtbagxon"
	$ ./configure --enable-libffmpeg_static --disable-nvenc

If any dependencies are missing the configure script will complain or attempt
to disable optional features.

Build the binary:

	$ make -j 6

After build, the binary resides in `build.linux` directory.

Thus, to start it, just type:

	$ ./build.linux/tvheadend

Settings are stored in `$HOME/.hts/tvheadend`.
