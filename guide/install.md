# Installing and Running the App

To join the Testnet you need to run the Spacemesh App on your desktop computer.

## About The Spacemesh App

The Spacemesh App (aka the App) includes a Spacemesh full p2p Node (which we call Smesher), and a basic Smesh wallet which we call Wallet.

### Smesher
Smesher is the software that creates and updates [the Smesh](../coins.md) (SMH) distributed ledger. It also creates and maintains your disk space commitment to the Spacemesh network. The Spacemesh decentralized platform is created by people just like you, who run a Smesher on their own desktop computers.

Your Smesher participates in the Spacemesh decentralized consensus Protocol and is responsible for the block-smeshing process. Block Smeshing is the process of submitting blocks with transactions to the Testnet network. You earn block smeshing rewards for submitting blocks with transactions to the Testnet network, according to the rules of the Spacemesh protocol.

Before you can produce blocks, you need to commit XXXX free storage on your computer hard drive to Spacemesh. The commitment process only happens once, when you set up your App, and is used indefinitely to produce more blocks. You will be prompted to start producing blocks and to commit disk storage when you run the Spacemesh App for the first time on your computer.

### Wallet
The Wallet is a basic Smesh (SMH) cons wallet that you use to maintain your Smesh (SMH) coins account, execute transactions and check the status of incoming transactions initiated by other accounts.

> For this release (Spacemesh 0.1), the Wallet works together with your locally-running Smesher and can't be used without running a Smesher in your computer. Future releases of the App will enable you to use the wallet without running a Smesher on your computer.

### App
The App integrates a Smesher and a Wallet into one package, which we hope you are going to find delightful and easy to use, even without having additional technical understanding of cryptocurrency terms and concepts.

> You do NOT need to run any additional software to join the Testnet, besides running the App on your computer.

---

Follow the instructions on this page to download, install and run the App.

## Step 1 - Downloading the Installer

> Before installing, please confirm that your computer meets the [minimum system requirements](requirements.md).

Next, download the App Installer for your OS using one of the links below:

### Windows 10

[Spacemesh Setup 0.0.4.exe](https://storage.googleapis.com/smapp/0.0.4/Spacemesh%20Setup%200.0.4.exe)

---

### OS X

[Spacemesh-0.0.3.dmg](https://storage.googleapis.com/smapp/0.0.4/Spacemesh-0.0.4.dmg)

---

### Linux

?> Debian 8 or newer, Ubuntu 12.04 or newer, Fedora 21 or newer, or any other flavor of linux which supports Electron apps are supported.

[smapp_0.0.3_amd64.deb](https://storage.googleapis.com/smapp/0.0.4/spacemesh_app_0.0.4_amd64.deb)


?> If your Linux system does not support Electron apps then you can build a Spacemesh full node and a CLI wallet from source code and join the Testnet. For more information see [go-spacemesh readme](https://github.com/spacemeshos/go-spacemesh)

---

### Security Notes

> All software released by Spacemesh is 100% open source. The App Installer you are downloading was packaged from code in the [Spacemesh Open Source Software Repos](https://github.com/spacemeshos) on github. We provide the Installer to make it convenient for non-developers to join the Spacemesh testnet.

> Follow [these steps](auth.md) if you'd like to verify that the Installer you have downloaded is authentic and has not been modified by a third party.

## Step 2 - Installing the App

**Locate the Installer you downloaded and double click it** to install the App.

### OS X
Drag the Spacemesh App icon in the installer window to the Applications folder shortcut. Next, open your Applications directory and double click `Spacemesh` to run it.

### Windows
Follow the on screen instructions. The installer defaults to launch Spacemesh as soon as it is the installation is complete.

> If you see a Windows security alert then check the checkbox 'Priave networks' and click 'Allow access'.

---

Next, [follow this guide](guide/setup.md) to set up a wallet and smeshing in the App.
