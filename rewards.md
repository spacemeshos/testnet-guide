# Smesh Rewards

Users who run the Smesher in the App and submit blocks to the network, are entitled to Smesh rewards.

> Learn more about [Smesh](coins.md).

## Rewards Account

Smesh rewards are awarded to the wallet main account that you have created in the App prior to setting up mining. This account is associated with your full node identity and is called the `Rewards Account`.

## Layers, Epochs and Blocks
Blocks with transactions are added into `layers`.

In the Spacemesh 0.1 Testnet, every layer has a constant time of 5 minutes.
Layers are numbered. The first layer after the Testnet goes live is  labeled `layer 0`, the next one `layer 1`, etc...

An `epoch` is a fixed number of layers. Each Testnet epoch has 288 layers and is 24 hours long.

So `Epoch 0` is the first 288 layers starting with `layer 0` and its last layer is `layer 287`, and `Epoch 1` start in `Layer 288` and ends with `Layer 575`.

Your eligibility to contribute blocks to a specific layer is determined by the Spacemesh protocol, and automatically executed by the App (as long as you haven't configured your Node to stop producing blocks).

The Spacemesh protocol guarantees that you will be eligible to submit at least one block in at least one layer in each and every epoch, once you have completed setting up your full Node and as long as your App is running.

## Layer Rewards
Each layer has a total reward of 50 Smesh. This reward is distributed to the rewards account of each miner who contributed at least one block to that layer.

So, for example, if a layer includes 10 blocks, each submitted by a different full node, 50 SMCH will be distributed evenly between the reward accounts of each of the 10 participating full nodes. Each account will be credited with 5 SMH.

## Layer Rewards Adjustment
This award amount is adjusted by the number of transactions included in blocks. The rewards for Smeshers which have submitted less than 15 transactions in their submitted block is reduced by 15%. This penalty is distributed as a bonus evenly to all full nodes who have submitted more than 15 transactions in their submitted block in the layer.

## Transaction-Fees
In addition to the layer award described above, all full nodes who submitted at least one block to a layer are entitled for a share of the transaction fees of valid transactions included in blocks in that layer.

The transaction fees in a layer, are evenly distributed to all the full nodes who have submitted a block in the layer.

## Tracking your Rewards
Rewards are added your rewards account when 4 layers (20 minutes) have passed since a layer that you are entitled to receive an award for.

To track your rewards, check your rewards account transactions log in the App.

TODO: add screen shot....


## Summary

- A fixed Smesh amount called the layer award is evenly distributed between all full nodes who contributed a block to the layer.

- The transaction fees of transactions included in a layer are evenly distributed between all full nodes who contributed a block to that layer.

- Full nodes who submit blocks with less than 15 transactions award is reduced. The penalty is shared between all full nodes who submitted blocks in that layer.
