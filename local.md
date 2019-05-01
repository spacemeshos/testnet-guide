# Local Testnet
You can setup and run a local Testent that consists 3 full nodes and the support services on your computer. This is a great way to get a feel of the platform. This guide is geared to developers who are comfortable with the command line and dev tools.

## Setup
Setup go development environment and docker. Clone go-spacemesh to your computer from github. Navigate to your go environment src folder and execute these commands:

```bash
mkdir src/github.com/spacemeshos
cd src/github.com/spacemeshos
git clone https://github.com/spacemeshos/go-spacemesh
```

## Building

Run this from the command line to build the local testnet docker images.

```bash
make local-testnet
```

This should create 4 docker images, one for every node and wallet, and one for the testnet services and symbolic links to the config file, the cli wallet and the log file of each node in the `build` folder:

Container 1 - Alice wallet + full node
Container 2 - Bob wallet + full node
Container 3 - Charlie wallet + full node
Container 4 - Services (poet, oracle)...

### Tree Structure Chart

- Build
    - local-net
        - node1 - Alice's node container
        - node2 - Bob's node container
        - node3 - Charlie's node container
        - node4 - services (poet, others)...
        - link to run Alice CLI wallet inside docker
        - link to run Bob CLI wallet inside docker
        - link to run Alice CLI wallet inside docker
        - link to view node1 console log
        - link to view node2 console log
        - link to view node3 console log
        - link to view node4 console log


## Running

```bash
cd build
./local-testnet.sh
```

### Exploring the config files
Each node has the same genesis configuration in their config file. Show how to look at the config file.

Each node has a configured CLI wallet. Show how to access the wallet cli for each node...


### Looking at node logs
You can see each node log output by...

# Executing a transaction

?> Show instructions how to use the CLI wallet in node 1 (Alice's wallet) to send 1 coin to Bob.

1. Access Alice CLI Wallet.
2. Type this to send 1 coin to Bob...
3. Query tx status from alice CLI Wallet...
4. Open Bob's CLI wallet and check the balance...
5. Look at any node log file and find the transaction confirmation...

# Doing more...

- Editing genesis data
- Restarting nodes
- Viewing mining awards balance in the wallet...
