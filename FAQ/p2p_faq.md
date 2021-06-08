# Testnet P2P Troubleshooting FAQ

## Do I need to configure my internet access point or firewall to be able to run a full p2p node?

As long as you have an active internet connection, Spacemesh should be able to communicate with the P2P network. This should even be enough for participating in the consensus protocol (Smeshing) and publishing transactions.

However, full nodes that are not reachable put a burden on the other nodes instead of strengthening the network.

To ensure that your node is reachable, the listening ports must be open and forwarded. To make this easy, the Spacemesh node uses technology called UPnP. You should verify in your router's settings that UPnP is enabled (in most cases it's on by default). If you can't turn it on, you should manually forward the ports used by Spacemesh (by default 7513 TCP and UDP) to the local computer running it.

## What ports does Spacemesh use?

TCP and UDP ports 7513. The port is configurable in 0.2 via the Smapp settings.
