# Setup Wallet + Mining

## Step 1 - Wallet Setup
Double-click the Spacemesh App Icon to launch it. You should now see this welcome screen:

![](../images/v1.0/welcome.png)

Let's now proceed to setup a Spacemesh full p2p mode, the mining process, and a Spacemesh Coins Wallet. But first - some definitions...

## About the Spacemesh Wallet
> A wallet holds one or more coin accounts. An account is identified by a long unique number such as `0x2012...0a1f`. It allows you to send and receive Spacemesh Coins and in the future run decentralized applications. Each account has a Spacemesh coins balance which you can spend.

Let's now setup a new wallet to manage your Spacemesh Coins and to provide your full p2p node with a `coins awards account`.

> A `coins awards account` is a wallet account you setup and use to receive Spacemesh Coins for running a Spacemesh full p2p node.

When setting up a full p2p node, your wallet main account will be used as the `coins awards account` for this full node.

?> Note that you can skip the full p2p node and the mining setup and run the Spacemesh App in `wallet-only mode`. This is useful if you only want to transact with Spacemesh Coins on your laptop when, for example, you run a Spacemesh full p2p node on your desktop. See [this guide](wallet_mode.md) for more info about this configuration.

---

Click on `SETUP` to start the setup process.

The next screen should look like this:

![](../images/v1.0/protect_wallet.png)

The App prompts you to enter a password to protect your new wallet and access to your Miner. Proceed to choose a password (8 or more characters) and to confirm it.

> You need to use the password to access your wallet after you lock access to the App. We recommend that you'll save your password in your computer's secure password manager.

> Until you backup your wallet, you will not be able to access it without your password. There is no way to restore a wallet that wasn't backed-up if you forget your password.

---

Click `NEXT`. You should now see this screen:

![](../images/v1.0/protect_wallet_confirmed.png)


## Step 2 - Full Node & Mining Setup

## About Spacemesh Mining
Spacemesh is using a novel consensus protocol which instead of constantly solving computational puzzles with your CPU, is using a one-time setup phase that utilizes free space on your hard drive.

The storage you commit defines your identity on the Spacemesh computer and determines your awards eligibility.

The more free disk space you commit, the more frequent your Spacemesh coin award frequency will be.

This setup is a one-time operation that you only need to do once and it allows Spacemesh to reach consensus on a distributed ledger without using proof of work or proof of stake algorithms.

The free space you commit to your full node is not used store any useful data files. It is filled with cryptographic data by the setup process that is only used to establish your node identity and your awards eligibility according the Spacemesh consensus protocol rules.

---

The Spacemesh App now prompts you to setup mining on your computer.

You need to specify which hard-drive you would like to use for mining and how much storage to allocate on that drive.

You should now see this screen:

![](../images/v1.0/miner_setup_drive.png)

Click on the hard-drive that you would like to use for mining and click 'NEXT':

You should now see this screen:

![](../images/v1.0/miner_setup_size.png)

Select on the amount of free space you would like to allocate to Spacemesh and click 'NEXT'.

> The more storage you allocate for Spacemesh on your drive, the higher your full node participations awards will be. (Add link to read more about POST commitments)

You should now see this screen:

![](../images/v1.0/miner_setup_complete.png)

> The one-time mining setup process is now started, and it may take 24-48 hours depending on your GPU capabilities. Do not turn off your computer until you get a notification about setup completion.

> The account currently selected in your wallet will be used as the `coins award address` for mining and full node awards.

Click 'GOT IT`.

---

## Step 3 - Desktop Computer Configuration

### Configure your Network
In order to participate in the Spacemesh network and earn mining awards you need to configure your computer firewall (and in some cases your home network router) so the Spacemesh App is able to accept incoming Internet connections on TCP port 7153 and on UDP port 7153.

Please follow the instructions in [this guide](netconfig.md).

### Disable Computer Sleep Mode
To finish the one-time mining process and to have your full node participate in the Spacemesh protocol and earn Spacemesh Coins awards **you need to make sure that your desktop computer doesn't not go to sleep or hibernates**.

Follow [this guide](no_sleep.md) to disable sleep on your computer.


## Next...
You are almost done! You are now ready to check your [Full Node Status](guide/status.md).
