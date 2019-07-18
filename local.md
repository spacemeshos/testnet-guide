# Spacemesh Local Testnet (Localnet)

![](https://spacemesh.io/content/images/2019/07/localnet_and_wallet.jpg)

👉 Follow this guide to build from source code and run a local Spacemesh Testent (localent) with 6 full nodes, 6 user accounts, and 1 POET support service on your computer using docker. This is a great way to get a feel for the protocol and the platform and to start hacking on Spacemesh.

!> The local testnet is an experimental alpha software in active development. It is built for developers who are comfortable with the command line, Docker, and dev env setup. You also need a strong modern dev computer to run it such as a Macbook Pro or a strong modern dev desktop computer. That said, we have tested it to work on all supported platforms and most of the issues we see are env setup.

## Youtube Video Tutorial

<iframe width="1280" height="720" src="https://www.youtube-nocookie.com/embed/IZvmzm8MzU8?rel=0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Prerequisites and Running
👉 OS X. Linux and Windows support is not fully tested yet.
👉 Follow the setup instructions in the local testnet repo [readme file](https://github.com/spacemeshos/local-testnet) to install the prerequisites and to build and run the testnet.

If all works as expected, you should have a terminal window which looks similar to this:

![local_net](https://spacemesh.io/content/images/2019/07/local_net.jpg)


?> Got stuck in setup? Got any questions? Join our [Gitter dev channel](https://gitter.im/spacemesh-os/Lobby) and get help.

## Working with the testnet

### Running the CLI Wallet
👉 Now when you have a local testnet is running on your computer - it is time to execute some transactions! Follow these instructions to execute transactions and check balances.

1. Open a new terminal window, navigate to CLIWallet directory in your go src directory.
```bash
cd $GOPATH/go/src/github.com/spacemeshos/CLIWallet
```
2. Run the wallet:
```bash
./CLIWallet
```

Your terminal window should now look similar to this:

![](/images/localnet_cliwallet.jpg)

### Viewing account balance

The localnet is pre-configured with 6 user accounts. Each of the 6 localnet full nodes has one of these account set as the mining award account. So full node mining awards will be periodically awarded to each of the user accounts.
When you launch the wallet you see a list of all pre-configured user accounts.

1. Enter `anton` to load Anton's account
2. Enter `account` to view Anton's information. You should see the account's name, balance and transactions nonce. The account balance is set in genesis

Your wallet terminal window open should look similar to this:

```
connected to node at  http://localhost:9090/v1
[gavrad tap yosher almog anton barak]
> choose one:
> almog
> anton
> barak
> gavrad
> tap
> yosher
$ anton
> Loaded account: anton pubkey: db58184012f26c405bff2d8866bf7ef2d1da7f0b391d1f1364f1d695929df617
$ account
<APP> INFO 001 10:55:12.886 ▶ Sending to url: http://localhost:9090/v1/nonce request : { "address": "0xdb58184012f26c405bff2d8866bf7ef2d1da7f0b391d1f1364f1d695929df617"}
<APP> INFO 002 10:55:12.901 ▶ resp: {"value":"0"} len 13
<APP> INFO 003 10:55:12.901 ▶ Sending to url: http://localhost:9090/v1/balance request : { "address": "0xdb58184012f26c405bff2d8866bf7ef2d1da7f0b391d1f1364f1d695929df617"}
<APP> INFO 004 10:55:12.905 ▶ resp: {"value":"10000"} len 17
> Name:  anton
> Balance:  10000
> Nonce:  0

```

### Executing a transaction

Now let's transfer 500 Spacemesh Coins (SMC) from `Anton` to `Yosher`
1. From Anton's wallet enter `transfer coins`. You should see a list of account
2. Enter `yosher` to send coins to yosher's account
3. Enter `500` to transfer 500 coins to transfer to yosher
4. Enter `n` when prompted about non-default gas price
5. Enter `y` to confirm the transaction

You should see this entry in the running localnet console window:
```
tx received by node, dst 0xF94Ab amount 500
```

It indicates that the transaction was received by a node.
Now wait for 3 to 4 layers to complete (about 3-4 minutes) until you see this entry in the localnet console output:

```
confirmed tx: orig: 0x66Bf7 dest: 0xF94Ab amount 500 nonce: 0
```

This entry indicates that the transaction was confirmed and that the global accounts state was updated to reflect it.

### Viewing updated account balances

Let's check `yosher` and `anton` balances in the CLI wallet and observe that they reflect the transaction amount.

1. Enter `account` to view Anton's current balance. It should reflect the executed transaction amount.

?> Note that as all user accounts are miner accounts of full nodes their balance will periodically increase due to epoch mining awards. This is why Anton's balance may be bigger than what you observed previously.

2. Enter `switch account` to switch an account.

3. Enter `yosher` to switch to view Yosher's account.

4. Enter `account` to view Yosher's balance.

> Yosher balance should now reflect the 500 coins he got from Anton plus any mining awards that he got for mining with his full node.

### Stopping the Testnet

👉  Just hit `ctrl-c` in the terminal window you started the Testnet from or close that terminal window.

👉  To close the CLI wallet Just hit `ctrl-d` or enter 'quit' or 'exit' in a running wallet instance terminal window.

### Connecting the wallet to a different node

TBR

### Hacking on the localnet

👉  The nodes genesis config is set using data from this file `genesis_accounts.json`. It is located in the root of the local testnet github repo you have cloned to your computer.

👉  The localnet log files are located in the `Logs` directory in the local testnet github repo root.


### Exploring config files

- Layers, miners, transactions and epochs....

----

?> Got stuck? Got any questions? Join our [Gitter dev channel](https://gitter.im/spacemesh-os/Lobby) and get help.
