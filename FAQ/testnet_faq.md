# General Testnet FAQ

## My node is synced. How long before I get rewards?

It can take up to 48 hours after syncing for your first smeshing rewards to come in.

## Is there a way to build a node using command-line?

Yes. We have a [CLI full-node](https://github.com/spacemeshos/go-spacemesh) and [CLIWallet](https://github.com/spacemeshos/cli-wallet), which is another way to run a Spacemesh full node instead of the Spacemesh App. Please be aware that this method is designed for users who are comfortable working with command line. If you have any questions about running a node via the CLI then please hit up the #cli channel on our discord.

## How do I report an issue?

First, check to see if the bug is known issue already under investigation by visiting our [bug reports repo](https://github.com/spacemeshos/bug-reports/issues). If it isn't, go to the #bug_reports channel on our [discord server](https://chat.spacemesh.io) and describe the bug. If applicable, a mod may ask you to submit your Spacemesh logs, which can be found by clicking the 'View Log' button in the settings of your app.

## Are testnet coins valid on mainnet/worth anything?

No, they are monopoly money without any real-world value, and not worth anything in real life.

## Will there be incentives/rewards for participating in testnet?

Not for 0.1. But there will be a rewards program launched after Spacemesh 0.2. Those rewards will not be mainnet coins, however.

## Is smeshing CPU-intensive?

The syncing phase of setting up a node can by quite CPU-intensive, but this should no longer be a problem once the node is synced.

## Why is my log file getting so big?

Since the purpose of the testnet is debugging, the log files can get quite large. However, *very* large log files (larger than a few gigabytes) usually mean there's some kind of issue with your node, so please notify us about it on the #bug_reports channel on discord.

If you wish to do log rotation, close the App first, compress your current log file before deleting it, then open the App again. A new log file will be created automatically.

## What's the purpose of the tap?

To test coin transactions and to give new testnet participants some coins to transact with before they win their first smeshing rewards.

## How many nodes can I run on the testnet?

As many as you like, but since testnet tokens have no value, there is no advantage to running more than one.

## Can I use a VPS/VM?

As long as it meets the [minimum requirements](requirements.md), yes. But we discourage users from doing so unless they are already using the VPS/VM for some other purpose as well.
