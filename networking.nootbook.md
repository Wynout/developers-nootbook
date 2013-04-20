# Networking

## Iperf
> [http://openmaniak.com/iperf.php](http://openmaniak.com/iperf.php)
Iperf is a tool to measure the bandwidth and the quality of a network link. The network link is delimited by two hosts running Iperf.


----------------

## Converting a TP-Link TL-WR1043ND to DD-WRT
[source](http://joeyiodice.com/converting-tp-link-tl-wr1043nd-to-dd-wrt)

Easy firmware with one catch.
If your router’s **Serial Number begins with **12, then you will need to **perform an additional step** before converting to DD-WRT.

The extra step is to flash a special german firmware image before flashing to DD-WRT.

Newer versions of the TL-WR1043ND router turn off the WAN port during a firmware upgrade which never gets turned back on in DD-WRT.

This special german firmware image prevents the WAN from being turned off during the DD-WRT conversion.

[source >> read more](http://joeyiodice.com/converting-tp-link-tl-wr1043nd-to-dd-wrt)


----------------


## DD-WRT - WDS multiple router setup
[source](http://www.dd-wrt.com/wiki/index.php/WDS_multiple_router_setup)

Multiple Routers can be setup with WDS, and the way that this is done is to set them up so they connect with adjacent routers. What this means is if your routers are in a line, you configure them to connect with only the one before and after them. Often enabling STP helps with connection issues. Here are the instructions that have worked for me:

[source >> read more](http://www.dd-wrt.com/wiki/index.php/WDS_multiple_router_setup)

----------------