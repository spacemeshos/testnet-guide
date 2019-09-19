# Full Node Coin Awards

## Coin Awards
People who run the Spacemesh full p2p node in the App, have setup mining and participate in the protocol by leaving their App running 24x7 are entitled to Spacemesh Coin awards.

## Coin Awards Accounts
Coin awards are awarded to the Wallet account you have created prior to setting up mining and is associated with your full node identity.

## Layers, Epochs and Blocks
Blocks with transactions are added by full p2p nodes into `layers`. Each layer has a constant time of 5 minutes. Layers are numbered. The first layer after the Testnet goes live (genesis) is  called `layer 0`, the next one is `layer 1`, etc...

An `epoch` is a fixed number of layers. Each Testnet epoch has XXX layers. So `Epoch 0` is the first XXX layers starting with `layer 0` and its last layer is `layer XXX-1`, and `Epoch 1` start in `Layer XXX` and ends with `Layer 2xXXX-1`.

Your eligibility to contribute blocks to a specific layer is automatically determined by the Spacemesh protocol.

The Spacemesh protocol guarantees that you will be eligible to submit at least one block and at least one layer in each and every epoch.

Each layer has a total award of 1 Spacemesh Coins. This award is distributed to the awards account of each miner who contributed at least one block to that layer.

So, for example, if a layer includes 10 blocks, each submitted by a different full node, 1 SMC will be distributed evenly between the coin awards accounts of each of the 10 participating full nodes. So each account will be credited with 0.1 SMCs.

This award amount is adjusted by the number of transactions included in blocks. The awards of full nodes who have submitted less than 15 transactions in their submitted block is reduced by 15%. This penalty is distributed as a bonus to all full nodes who have submitted more than 15 transactions in their submitted block.

## Transaction Fees
In addition to the block award described here, all full nodes who submitted at least one block to a layer are awarded with the transactions fees of valid transactions included in that layer.

The transaction fees in a layer, are evenly distributed to all the full nodes who have submitted a block in the layer.

## Tracking your Awards
Awards are added your awards account when 5 layers have passed since a layer that you are entitled to receive awards for.

Check your awards account transaction logs in the App to track your awards.

TODO: add screen shot....
