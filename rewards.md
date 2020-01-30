# Smesh Rewards

## Overview
Users who run the Smesher in the App and submit blocks to the network, are entitled to Smesh rewards. After setting up smeshing on your computer you should get your first reward in up to 49 hours.  Starting with the time of your first reward, you should start getting a reward every 24 hours.

Every 5 minutes time period, the protocol distributes 50 Smesh (SMH) to all smeshers who contributed one or more block to the mesh in the time period.

Your exact reward amount depends on how many smeshers added blocks to the mesh in that time period. Keep reading this page for a more detailed technical explanation.



> Learn more about [Smesh (SMH)](coins.md) coin units.

---

## Rewards Account

Smesh rewards are rewarded to the wallet main account that you have created in the App prior to setting up mining. This account is associated with your Smesher's identity and is called the `Rewards Account`.

## Layers, Epochs and Blocks

Blocks with transactions are added into `layers`.

In the Spacemesh 0.1 Testnet, every layer has a constant duration of 5 minutes.
Layers are numbered. The first layer after the Testnet goes live is labeled `layer 0`, the next one `layer 1`, etc...

An `epoch` is a fixed number of layers. Each Testnet epoch has 288 layers and is 24 hours long. So, `Epoch 0` is the first 288 layers starting with `layer 0` and its last layer is `layer 287`, and `Epoch 1` start in `Layer 288` and ends with `Layer 575`.

Your eligibility to contribute blocks to a specific layer is determined by the Spacemesh protocol, and automatically executed by the App (as long as you haven't configured your Smesher to stop smeshing blocks).

The Spacemesh protocol guarantees that you will be eligible to submit at least one block in at least one layer in each and every epoch, once you have completed setting up your Smesher and as long as your App is running.

## Layer Rewards
Each layer has a total reward of 50 Smesh. This reward is distributed to the rewards account of each miner who contributed at least one block to that layer.

So, for example, if a layer includes 10 blocks, each submitted by a different Smesher, 50 SMH will be distributed evenly between the reward accounts of each of the 10 participating Smeshers. Each account will be credited with 5 SMH.

## Layer Rewards Adjustment
This reward amount is adjusted by the number of transactions included in blocks. The rewards for Smeshers which have submitted less than 15 transactions in their submitted block is reduced by 10%. This penalty is distributed as a bonus evenly to all Smeshers who have submitted more than 15 transactions in their submitted block in the layer.

## Transaction-Fees
In addition to the layer reward described above, all Smeshers which submitted at least one block to a layer are entitled for a share of the transaction fees of valid transactions included in blocks in that layer.

The transaction fees in a layer, are evenly distributed to all the Smeshers who have submitted a block in the layer.

## Tracking your Rewards
Rewards are added your rewards account when 4 layers (20 minutes) have passed since a layer that you are entitled to receive a reward for.

To track your rewards, check your rewards account transactions log in the App.

TODO: add screen shot....


## Summary

- A fixed Smesh amount called the layer reward is evenly distributed between all Smeshers which contributed a block to the layer.

- The transaction fees of transactions included in a layer are evenly distributed between all the Smeshers that contributed a block to that layer.

- Smeshers which submit blocks with less than 15 transactions reward is reduced. The penalty is shared between all Smeshers who submitted blocks in that layer.
