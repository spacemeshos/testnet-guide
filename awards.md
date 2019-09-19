# Full Node Coin Awards

People who run the Spacemesh full p2p node in the App, have setup mining and participate in the protocol by leaving their App running 24x7 are entitled to Spacemesh Coin awards.

Coin awards are awarded to the Wallet account you have created prior to setting up mining and is associated with your full node identity.

Blocks with transactions are added by full p2p nodes in `layers`. Each layer has a constant time of 5 minutes. Layers are numbered. The first layer after the Testnet goes live is `layer 0`, the next one is `layer 1`, etc...

An `epoch` is a fixed number of layers. Each epoch has XXX layers. So Epoch 0 is the first XXX layers starting with `layer 0` and its last layer is `layer XXX-1`.

Your eligibility to contribute blocks to a specific layer is automatically determined by the Spacemesh protocol.

The Spacemesh protocol guarantee that you will be eligible to submit at least one block and at least one layer in every epoch.

Each layer has a total award of 1 Spacemesh Coin. This award is distributed to the awards account of each miner who contributed blocks to that layer.

So, for example, if a layer includes 10 blocks, each submitted by a different full node, 1 SMC will be distributed evenly between the coin awards account of each of the 10 participating full nodes. So each account will be credited with 0.1 SMCs.

This amount is adjusted by the number of transactions included in blocks. The awards of full nodes who have submitted less than 15 transactions in their block is reduced by 15%. This penalty is distributed as a bonus to all full nodes who have submitted more than 15 transactions in their block.

In addition to the block award described here, all full nodes who submitted at least one block to a layer get the transactions fees of valid transactions included in that layer. The transaction fees are evenly distributed to all the full nodes who have submitted a block in the layer.
