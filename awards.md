# About Coin Awards

## Coin Awards
Users who run the Spacemesh full p2p node in the App, have set up mining and participate in the Spacemesh consensus protocol by leaving their App running 24/7 are entitled to `Spacemesh Coin awards`.

> Learn more about [Spacemesh Coin Units](smc.md).

## Coin Awards Account

Coin awards are awarded to the wallet main account that you have created in the App prior to setting up mining. This account is associated with your full node identity and is called the `Coin Awards Account`.

## Layers, Epochs and Blocks
Blocks with transactions are added into `layers`.

In the Testnet, every layer has a constant time of XXX minutes.
Layers are numbered. The first layer after the Testnet goes live is  labeled `layer 0`, the next one `layer 1`, etc...

An `epoch` is a fixed number of layers. Each Testnet epoch has XXX layers.

So `Epoch 0` is the first XXX layers starting with `layer 0` and its last layer is `layer XXX-1`, and `Epoch 1` start in `Layer XXX` and ends with `Layer 2xXXX-1`.

Your eligibility to contribute blocks to a specific layer is determined by the Spacemesh protocol, and automatically executed by the App.

The Spacemesh protocol guarantees that you will be eligible to submit at least one block in at least one layer in each and every epoch.

## Layer Awards
Each layer has a total award of 1 Spacemesh Coins. This award is distributed to the awards account of each miner who contributed at least one block to that layer.

So, for example, if a layer includes 10 blocks, each submitted by a different full node, 1 SMC will be distributed evenly between the coin awards accounts of each of the 10 participating full nodes. Each account will be credited with 0.1 SMC.

## Layer Awards Adjustment
This award amount is adjusted by the number of transactions included in blocks. The awards for full nodes who have submitted less than 15 transactions in their submitted block is reduced by 15%. This penalty is distributed as a bonus evenly to all full nodes who have submitted more than 15 transactions in their submitted block in the layer.

## Transaction-Fee Awards
In addition to the layer award described above, all full nodes who submitted at least one block to a layer are entitled for a share of the transaction fees of valid transactions included in blocks in that layer.

The transaction fees in a layer, are evenly distributed to all the full nodes who have submitted a block in the layer.

## Tracking your Awards
Awards are added your awards account when 5 layers have passed since a layer that you are entitled to receive an award for.

Check your awards account transaction logs in the App to track your awards.

TODO: add screen shot....

## Summary

- A fixed SMC amount called the layer award is evenly distributed between all full nodes who contributed a block to the layer.

- The transaction fees of transactions included in a layer are evenly distributed between all full nodes who contributed a block to that layer.

- Full nodes who submit blocks with less than 15 transactions award is reduced. The penalty is shared between all full nodes who submitted nodes with more than 15 transactions in that layer.
