# Installing and Running

Follow this guide to download, install and run a Spacemesh Testnet full node and wallet on your desktop computer.

## Step 1 - Downloading the Installer

The Spacemesh App includes the Spacemesh full node, a basic wallet and a full node dashboard. You install the App to setup your p2p node and you use the wallet to setup an award account for your full node.

Before installing, please confirm that your system meets the [minimum system requirements](requirements.md).

Next download the App installer for your OS using on of the links below:

### OS X

[SPACEMESH_OS_X_INSTALLER](dmg_installer)

---

### Windows 10

[SPACEMESH_WIN10_INSTALLER](exe_installer)

---

### Debian Linux

?> Debian 8 or newer is supported

[SPACEMESH_DEB_INSTALLER](deb_installer)

---

### Ubuntu or Fedora Linux

?> Ubuntu 12.04 or newer and Fedora 21 or newer are supported

[SPACEMESH_UBUNTU_INSTALLER](AppImage_installer)

---

### Other Flavors of Linux

?> Running a linux distribution that doesn't support Electron apps? We got you covered! Just follow [this guide](linux.md) to join the Testnet from your system.

---

### Security Note

The installer you are downloading was packaged from code in the [Spacemesh open source software repos](https://github.com/spacemeshos) on github and all software released by Spacemesh is 100% open source.

We provide these installers in order to make it convenient for non-developers to join Spacemesh. If you prefer and technically able, you can build and run the installer [directly from source code](build.md) instead of using our provided installer.

## Step 2 - Running the App

First follow [these steps](auth.md) to verify that the Installer you have downloaded is authentic and not has not been modified by a 3rd party.

Next, **locate the installer you downloaded and double-click it**.

---

## Step 3 - Creating a Wallet

You should now see the app's welcome screen.

![](../images/welcome.png)

You will now setup a new wallet to manage your Spacemesh Coins and to provide your full node with a `coins awards address`.

?> A `coins awards address` is where you receive Spacemesh Coins for running a full node.

You also use your wallet to send coin to anyone and to receive coins from anyone.

Click `Start Setup`.

![](../images/wallet_passphrase.png)

The App prompts you to enter a passphrase to protect your new wallet. Proceed to choose a passphrase and to confirm it.

!> You will need to use the passphrase to access your wallet after you close the App. We recommend that you'll save your passphrase in your computer's secure password manager.

!> Until you backup your wallet, you will not be able to access it without your passphrase. There is no way to restore a wallet that wasn't backed-up if you forget your passphrase.

### About your Wallet

![](../images/wallet.png)

Your new main wallet is configured with a new `default address`. Each address has Spacemesh Coin balance that you can spend.

You can create additional addresses later, but for now, you will use this address as the address for coin awards that will be awarded to you for running a full node on your computer.

Coin awards will appear in the balance of this address in your wallet.

The setup automatically configures your full node with your `default address`. You can change the full node award address later and at any time in the App.

---

## Well Done!

Now that you have a new wallet and a new `default address`, you are ready to [setup your Spacemesh full node...](guide/setup.md)
