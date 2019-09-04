## Spacemesh Full Node and App Requirements

!> Note that the requirements below are tentative and are subject to change pending further testing.

#### Minimum System Requirements

- A computer with modern Intel or AMD multi-core CPU (2 or more cores)
- OS X, Windows 10, Ubuntu 12.04, Fedora 21, Debian 8
- 4GB RAM
- 150GB free space on a magnetic hard-drive or SSD drive
- An always on unmetered broadband Internet connection
- Internet connection speed. (Download: 5 mbps. Upload: 1 mbps)
- Configuration to accept incoming Internet connections to a port

---

#### Recommended System Requirements

- Desktop computer with modern Intel or AMD multi-core CPU (4 or more cores)
- OS X, Windows 10, Ubuntu 12.04 or newer, Fedora 21 or newer, Debian 8 or newer
- 8 GB RAM
- 150GB free space on a magnetic hard-drive or SSD drive
- An always on unmetered broadband Internet connection
- A modern AMD or Nvidia GPU with OpenCL support
- Internet connection speed. Download: 10 mbps. Upload: 1 mbps.
- Configuration to accept incoming Internet connections to a port

---

### Operational Notes

#### GPU Usage

It is possible to setup a Spacemesh full node on a system without a GPU, but in this case, the setup phase will take up to x100 longer than with the same system with a GPU supporting OpenCL.

A fast GPU considerably reduces a Spacemesh full node one-time setup phase duration. Your GPU is not used by the full node after the one-time setup phase.

By default, not all of your GPU cores are used during the one-time setup phase, so you should be able to use your PC as you normally do during the setup phase.


#### CPU Usage
As long as your system and configuration meets the recommended  requirements, the Spacemesh Full Node and App ongoing usage of your CPU should be limited during normal operation (after the initial setup phase) to one CPU core.

#### Network Configuration
You must configure your network to allow the Spacemesh App to accept incoming connections. See [this guide](netconfig.md)

#### Running a Full Node on your Laptop
You can install and run a full node on it if it meets the minimum desktop computer requirements. However, you will need to make sure you leave it open and connected to power and the Internet 24x7. Occasionally shutting down your full node may prevent you from participating in consensus and earning coin awards.

---

### Spacemesh App (Wallet-only Mode) System Requirements

You can use the Spacemesh App wallet features without running a full node on your laptop or desktop computer. This configuration requires a modern laptop or desktop computer running OS X, Windows 10, Ubuntu 12.04 and newer, Fedora 21 or Debian 8.

#### Wallet-only Setup
Follow these steps to setup your wallet without running a full node
1. [Install the Spacemesh App](guide/install.md) on your computer and run it
2. Click `Maybe Later` when prompted to setup a full node
3. Click on the `Wallet command` in the main screen to access your Wallet
4. Learn about [using your wallet](wallet.md)
---

### Linux Support
?> The Spacemesh App is an Electron App. It is supported on any Linux distro that supports [Electron apps](https://electronjs.org/docs/tutorial/support).

If you are running another flavor of Linux then you can install the Full Node Linux Distro which includes the full node and a CLI wallet. Alternative your may build and run a full node and a CLI wallet from source code. [Learn more...](linux.md)

You may also run the Full Node and the CLI wallet inside a docker container. [Learn more](docker.md)...
