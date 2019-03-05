# Spacemesh Full p2p Node Operational Requirements (Testnet release)

Note that the requirements below are tentative and are subject to change pending further testing.

#### Minimum System Requirements
- Desktop computer with modern Intel or AMD multi-core CPU (2 or more cores)
- 4GB RAM
- 150GB free space on a magnetic hard-drive or SSD drive (1)
- An always on unmetered broadband Internet connection
- OS X, Windows 10, Ubuntu 12.04 or newer
Fedora 21, Debian 8
- Internet connection speed. Download: TBD mbps. Upload: TBD mbps
- Configuration to accept incoming Internet connections to a port

#### Recommended System Requirements
- A modern AMD or Nvidia GPU with OpenCL support (2)
- 16 GB RAM
- 4 or more CPU cores
- Internet connection speed. Download: TBD mbps. Upload: TBD mbps.

#### Operational Requirements
1. As long as a user's system and configuration meet the recommended system requirements, the Full Node use of CPU should be limited during normal operation (post the initial setup phase) to one CPU core
2. By default, not all GPU cores should be used during the setup phase, so the user is able to use its PC for playing games.

(1) Subject to change pending further testing
(2) A modern GPU considerably reduces a Spacemesh full node setup time. It is possible to setup a Spacemesh full node on a system without a GPU, but in this case, the setup phase will take up to x100 longer than with the same system with a GPU supporting OpenCL

# Spacemesh App (Wallet Only Mode) Requirements
You can use the Spacemesh App wallet features without running a full node on your computer.

This configuration requires just a modern computer running OS X, Windows 10, Ubuntu 12.04 and newer, Fedora 21 or Debian 8.

# Linux support
Spacemesh App distribution (Full Node + GUI Wallet + Full Node Dashboard) is supported on any Linux distro that supports [Electron apps](https://electronjs.org/docs/tutorial/support).

If you are running another flavor of Linux then you can install the `Full Node Linux Distro` which includes the full node and a CLI wallet, or build and run the full node and CLI wallet from source code. You may also run the Full Node and the CLI wallet inside a docker container.
