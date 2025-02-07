# bitcoin-private-nodes

A curated list of Bitcoin full nodes running as **Tor v3 onion services** and **I2P nodes**.

This list can serve as a useful **bootstrap source** for nodes operating exclusively over privacy networks.  

These nodes have been observed at a given point in time, but **availability is not guaranteed**.

Currently, the list contains **X onion nodes** and **Y I2P nodes**.

## 🚀 How to use the node list

To connect your bitcoind instance using this list, add the following lines to your bitcoin.conf file:

Tor-only example:

```
addnode=abcd1234example.onion:8333
addnode=xyz9876example.onion:8333
```

I2P-only example:

```
addnode=mnop5678example.b32.i2p:8333
addnode=qrs5432example.b32.i2p:8333
```

After restarting your node, it will attempt to connect to these peers.

Over time, your node will discover additional peers through normal operation.
