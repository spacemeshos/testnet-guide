# Local Testnet

Follow this guide to setup and run a local Spacemesh Testent with 3 full nodes and support services on your computer using docker. This is a great way to get a feel of the protocol and the platform.

?> This guide is geared to developers who are comfortable with the command line, Docker and dev tools.

## Setup
👉 First, set up your go development environment and docker. Next, Git clone go-spacemesh to your Linux or OS X system. Windows is not yet supported.

```bash
mkdir $GOPATH/src/github.com/spacemeshos
cd $GOPATH/src/github.com/spacemeshos
git clone https://github.com/spacemeshos/go-spacemesh
```

## Building

👉 Now let's build a local testnet with 3 full nodes, 3 end-users and supporting services. Run this from the command line to build the local testnet artifacts:

```bash
make local-net
```

?> This command builds all artifacts, creates 4 docker images, one for each of the 3 full nodes, and one image for the testnet services. It also creates symbolic links to each of the node's config file, and associated cli wallet and the log file of each node in the `build/local-net` folder.

When the command finishes, your `build/local-net` folder should look similar to this:

```
- Build/local-net
    - nodeAlice.img - Alice's node container image
    - nodeBob.img - Bob's node container image
    - nodeCharlie.img - Charlie's node container image
    - services.img - services (poet, others) container image

    - alice_wallet.lnk - link to run Alice CLI wallet inside docker
    - bob_wallet.lnk - link to run Bob CLI wallet inside docker
    - charlie_wallet.lnk - link to run Alice CLI wallet inside docker

    - nodeAlice.log - link to view node1 console log
    - nodeBob.log - link to view node2 console log
    - nodeCharlie.log - link to view node3 console log
    - services.log - link to view node4 console log

    - nodeAlice.conf - link to Alice's node config file
    - nodeBob.con - link to Bob's node config file
    - nodeCharlie.conf - link to Charlie's node config file

    - start.sh - script to start the testnet
    - stop.sh - script to stop the testnet
```

## Running

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
