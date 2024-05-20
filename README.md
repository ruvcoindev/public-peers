                                                         Public Peers.
This repository contains peering information for publicly accessible nodes on the Ruvchain network. 
This repo only for Ruvchain v0.5.5 peers.

Note that not all peers in this repository are guaranteed to be online - check the Public Peers page instead to find peers that are online now.

In most cases, public peers should be accessible by adding the string provided for each peer to the Peers: [] section of your ruvchain.conf configuration file.

Example in ruvchain.conf:

Peers:
[
  tcp://a.b.c.d:e
  tcp://d.c.b.a:e
  tcp://[a:b:c::d]:e
  tcp://[d:c:b::a]:e
]

How do I pick peers?
If you are new to the network then take a look at the Public Peers page to find public peers that are online.

Always try to pick peers that are as close to you geographically as possible, as this will keep the latency of the network down.

If you are using a home connection then you should avoid peering with any nodes that are far away, as you may end up carrying traffic for the rest of the network.

For normal usage, you probably only need 2 or 3 peers.

                                                              TLS peers.
As of Ruvchain v0.5.5, peering connections over TLS are now possible. This hides the peering connection inside a regular TLS session, which can help in some cases where firewalls or deep packet inspection may identify or block regular Ruvchain peering traffic.

TLS public peers are identified by the prefix tls:// instead of tcp://.

Note that, due to the additional layer of encryption, performance via TLS peers may be slightly worse than via regular tcp:// peers.
