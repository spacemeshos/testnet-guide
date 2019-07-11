# Local Testnet

Follow this guide to build from source and run a local Spacemesh Testent (localent) with 6 full nodes and the POET support service on your computer using docker. This is a great way to get a feel for the protocol and the platform and to start hacking on Spacemesh.

?> This guide is for developers who are comfortable with the command line, Docker and dev tool chains.

## Prerequisites and Running
👉 Follow the instructions in the local testnet repo [readme file](https://github.com/spacemeshos/local-testnet) to install the prerequisites and to build and run the testnet.

## Working with the testnet
👉 Now when you have a local testnet is running on your computer - it is time to execute some transactions.
Follow these instructions to execute transactions and check balances.

1. Navigate to CLIWallet directory in your go src directory.
```bash
cd ~/go/src/github.com/spacemeshos/CLIWallet
```
2. Run the wallet.
```bash
./CLIWallet
```



------

Running
👉 Run this script to start the local net:

```bash
./build/local-net/start.sh
```

When this script execution is complete, you should the following running docker containers:

```
- nodeAlice.ctr - Alice wallet + full node
- nodeBob.ctr - Bob wallet + full node
- nodeCharlie.ctr - Charlie wallet + full node
- services.ctt - Services (poet, oracle)...
```

### Exploring the config files
Each node has the same genesis configuration in their config file. Show how to look at the config file. Each node has a configured CLI wallet.

👉 click on one of the links to view each node's config file:

```
- nodeAlice.conf - link to Alice's node config file
- nodeBob.conf - link to Bob's node config file
- nodeCharlie.conf - link to Charlie's node config file
```

# Nodes Setup

!> We need to provide instructions how to setup POST for each node or automatically set POST and submit ATXs when the local testnet starts and explain this...


### Looking at node logs
👉  You can see each node log output by...

```
- nodeAlice.log - link to view node1 console log
- nodeBob.log - link to view node2 console log
- nodeCharlie.log - link to view node3 console log
- services.log - link to view node4 console log
```

# Checking Account Balance

👉 Start the CLI wallet for Alice:

```bash
./build/local-net/alice_wallet.lnk
```

```bash
TODO: wallet command here to unlock it and output the balance
```

?> You can view Bob's and Charlie's balance in a similar manner.
Alice should have 10, Bob 9 and Charlie 8 Spacemesh Coins.

# Executing a transaction

?> Show instructions how to use the CLI wallet in node 1 (Alice's wallet) to send 1 coin to Bob.

1. Access Alice CLI Wallet.
2. Type this to send 1 coin to Bob...
3. Query tx status from alice CLI Wallet...
4. Open Bob's CLI wallet and check the balance...
5. Look at any node log file and find the transaction confirmation...
6. Check mining awards....

# Stopping

To stop the local net run this script:

```bash
./build/local-net/stop.sh
```

# Doing more...
- Editing genesis data
