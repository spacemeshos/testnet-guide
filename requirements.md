## Spacemesh App Requirements

!> Note that the requirements below are tentative and are subject to change pending further testing.

### Minimum System Requirements

- A computer with modern Intel or AMD multi-core CPU (2 or more cores)
- OS X, Windows 10, Ubuntu 12.04, Fedora 21, Debian 8
- 4 GB RAM
- 150 GB free space on a magnetic hard-drive or SSD drive
- An always on unmetered broadband Internet connection capable of 5 mbps downloads and 1 mbps uploads.
- Network Configuration that allows the App to accept incoming Internet connections on UDP port 7153 and TCP port 7153

---

### Recommended System Requirements

- A desktop computer with modern Intel or AMD multi-core CPU (4 or more cores)
- OS X, Windows 10, Ubuntu 12.04 or newer, Fedora 21 or newer, Debian 8 or newer
- 8 GB RAM
- 150 GB free space on a magnetic hard-drive or SSD drive
- An always on unmetered broadband Internet connection
- A modern AMD or Nvidia GPU (for GPU mining)
- An always on Internet connection capable of 10 mbps downloads and 1 mbps uploads.
- Network Configuration that allows the App to accept incoming Internet connections on UDP port 7153 and TCP port 7153

---

## Operational Notes

### GPU Usage

>The first version of the App does not perform GPU mining and uses the CPU for mining.

The following notes are only relevant once we release an App update with GPU mining support.

It is possible to setup the Spacemesh Miner on a system without a GPU, but in this case, the setup phase may take up to x100 longer than with the same system with a supported GPU.

A fast GPU considerably reduces the Spacemesh Miner one-time setup phase duration. Your GPU is not used by the App after the one-time setup phase is complete.

By default, not all of your GPU cores are used during the one-time setup phase, so you should be able to use your PC as you normally do during the setup phase.


### CPU Usage
As long as your system and configuration meets the recommended  requirements, the Spacemesh App ongoing usage of your CPU should be limited during normal operation (after the initial setup phase) to two CPU cores.

### Network Config
You must configure your network to allow the Spacemesh App to accept incoming connections on UDP port 7153 and on TCP port 7153. Follow [this guide](netconfig.md) to configure your network.

### Running the App on your Laptop
You can install the App, run a full p2p node and mine on your laptop if it meets the [minimum desktop computer requirements](requirements.md).

However, you will need to make sure you leave your laptop open and connected to power and to the Internet 24x7.

Occasionally shutting down your laptop or the App may prevent you from participating in consensus and earning participation coin awards.

You can also use your laptop to install the app and run it in [wallet only mode](wallet_mode.md)

---

### Wallet-only Mode System Requirements

> You can use the Spacemesh App wallet features without mining and without running a full node on your laptop or desktop computer. We call this wallet-only mode.

This configuration requires a modern laptop or a desktop computer running OS X, Windows 10, Ubuntu 12.04 and newer, Fedora 21 or Debian 8 with minimum 4GB of RAM. You do not need any specific GPU to run in wallet only mode as in this mode there is no mining or a running full p2p node in the App.

Learn more about the [Wallet Only App Mode](wallet_mode.md).

---

### Linux Support
> The Spacemesh App is an Electron App. It is supported on any Linux distro that supports [Electron apps](https://electronjs.org/docs/tutorial/support).

If your Linux system doesn't support Electron Apps then you can build and run a full p2p2 node and a CLI wallet using the instructions in  [this guide](build.md).

You may also run the Full Node and the CLI wallet inside a docker container on any system which supports docker. [Learn more](docker.md)...
