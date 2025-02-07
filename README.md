# bitcoin-private-nodes

A curated list of Bitcoin full nodes running as **Tor v3 onion services** and **I2P nodes**.  
This list can serve as a useful **bootstrap source** for nodes operating exclusively over privacy networks.  

These nodes have been observed at a given point in time, but **availability is not guaranteed**.

Currently, the list contains **X onion nodes** and **Y I2P nodes**.

## 📌 Why does this list exist?

When setting up a **privacy-focused Bitcoin node**, finding peers can be challenging—especially if you want to operate entirely over **Tor** or **I2P**.  

Bitcoin’s built-in peer discovery works, but it can be slow for hidden services.  
This list provides **known peers** to help new nodes quickly establish initial connections.

## 🔍 How is this list generated?

These addresses are collected using periodic queries to a running Bitcoin node:

```bash
bitcoin-cli getpeerinfo
```

No special techniques—just simple observation of reachable nodes.

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
