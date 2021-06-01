# General Testnet FAQ

## My node is synced. How long before I get rewards?

It can take up to 48 hours (2 testnet epochs) after syncing for your first smeshing rewards to come in.

## Is there a way to build a node using command-line?

Yes. We have a [CLI full-node](https://github.com/spacemeshos/go-spacemesh) and [CLIWallet](https://github.com/spacemeshos/cli-wallet). and you can join the testnet using them instead of with the Spacemesh App.Please be aware that these products are designed for people who are comfortable with command line apps. If you have any questions about running a node via the CLI then please hit up the #cli channel on our discord.

## How do I report an issue?

First, check to see if the bug is known issue already under investigation by visiting our [bug reports repo](https://github.com/spacemeshos/bug-reports/issues). If it isn't, go to the #bug_reports channel on discord and describe the bug. If applicable, a mod may ask you to submit your Spacemesh logs, which can be found by clicking the 'View Log' button in the settings of your app.

## Are testnet coins valid on mainnet/worth anything?

No, they are monopoly money without any real-world value, and not worth anything in real life.

## Will there be incentives/rewards for participating in testnet?

Not for 0.1. But there will be a rewards program launched after Spacemesh 0.2. Those rewards will not be mainnet coins, however.

## What's the purpose of the tap?

To test coin transactions and to give new testnet participants some coins to transact with before they win their first smeshing rewards.

## Can you transfer the node's sync status from one machine to another?

In theory it should work fine. You just need to copy the database directory (the one specified on the command line with --datadir or -d), and the wallet file. It's more likely to work on the same platform (e.g., Linux to Linux) and is not guaranteed to work across platform (e.g., Windows to Linux) - but it might work cross-platform too.

## How many nodes can I run on the testnet?

As many as you like, but there is no advantage to running more than one.

## Can I use a VPS/VM?

As long as it meets the [minimum requirements](requirements.md), yes. But we discourage users from doing so unless they are already using the VPS/VM for some other purpose as well.
