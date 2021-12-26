## Spacemesh 0.2 System Requirements

Updated for Spacemesh 0.2 Beta 2 release.

### Spacemesh App Requirements
The following are the requirements for running the Spacemesh App with a managed full Spacemesh node.

#### Minimum System Requirements

- A computer with modern Intel or AMD x86-64 CPU (3 cores / 6 native threads).
- OS: Windows 10 (Home or Pro), macOS, Ubuntu 18.04, Fedora 21, or Debian 8.
- 8 GB RAM.
- 150 GB free space. (HDD or SSD).
- An always-on, unmetered Internet connection capable of 5 mbps download and 1 mbps upload.

#### Recommended System Requirements

- A desktop computer with modern Intel or AMD x86-64 CPU (4 cores / 8 native threads or better).
- OS: Windows 10 (Home or Pro), macOS, Ubuntu 20.04, Fedora 21, or Debian 8.
- 16 GB RAM.
- 350GB free space. (HDD or SSD).
- An always-on, unmetered Internet connection capable of 10 mbps download and 1 mbps upload.

#### Linux Systems
> The Spacemesh App is an Electron App. It is supported on any Linux distribution that supports [Electron apps](https://electronjs.org/docs/tutorial/support).

#### Supported Processors for proof of space setup

You can create proof of space data using your computer's integrated graphics card, a discrete graphics card, or your computer's main CPU. The following processors are supported:

- A modern Intel or AMD x86-64 cpu.
- An Nvidia GPU with CUDA support (minimum compute compatibility 5.0, maximum compute compatibility 8.6), and Nvidia drivers version R450 or newer. [Nvidia GPUs CUDA compute compatibility info](https://developer.nvidia.com/cuda-gpus).
- A GPU and drivers with Vulkan 1.2 support, such as a modern AMD, Apple M1, and Intel GPUs.

#### Popular Supported Processors Models

- Nvidia Geforce RTX 2070 / 2080.
- Nvidia GTX 1060.
- AMD Radeon RX [550](https://www.newegg.com/onda-model-rx550-4g/p/1DW-00C1-00001) / 570 / 580.
- AMD Radeon Pro 555x.
- Nvidia Tesla V100, T4, P100 or P4.
- Apple M1.
- Intel UHD Graphics 630.


## Operational Notes

### CPU Usage
As long as your system and configuration meets the recommended requirements, ongoing utilization of your CPU by the Spacemesh App should be limited during normal operation (after the initial setup phase) to 2 CPU cores.

### Network Configuration
Your network should allow the App to accept incoming connections on UDP port 7153 and on TCP port 7153 and your computer firewall should not block incoming UDP and TPC packets on this port. The App attempts to automatically configure your network using UPnP. In some cases you may need to configure your router and firewall manually. Follow [this guide](netconfig.md) to configure your network.

### Laptop Usage
You can install the App, run a Smesher and produce blocks on your laptop if it meets the minimum system requirements. However, you will need to make sure you leave your laptop open and connected to power and to the Internet 24/7.

Occasionally shutting down your laptop or the App may prevent you from Smeshing blocks and from earning Smeshing rewards.

### Spacemesh Full Node Sysmte Requirements

Following are the requirements for running the a Spacemesh 0.2 full node without running the Spacemesh App. We recommend this setup to technical users who are comfortable with the command line.

> With this setup, your computer will be dedicated to running the Spacemesh full node and will not be used for running other interactive apps.

- A computer with a modern Intel, an AMD CPU (2 cores / 4 native threads) or an Apple M1 CPU.
- Windows 10 Home or Pro, macOS, Ubuntu 18.04, Fedora 21, or Debian 8.
- 4 GB RAM.
- 300 GiB free disk space (HDD or SSD).
- One of the supported processors for proof of space setup.
- An always-on, unmetered Internet connection capable of 10 mbps download and 1 mbps upload.

---

### About Proof of Space Data

You only need to setup proof of space data once to smesh for an unlimited period of time. The proof of space data size for the Spacemesh 0.2 testnet is `2 KiB`, `3 KiB` or `4 KiB`. The larger your proof of space data is, the higher your smeshing rewards will be.

> Upcoming Spacemesh Testnets will use closer to mainnet data sizes. The proof of space data size range for these upcoming testnets has not been finalized yet.

You can use any magnetic hard drive (HDD) or SSD drive for storing proof of space data. There is no significant advantage in using an SSD over HDD.

You do not need to have temporary disk space larger than your final proof of space data. Creating proof of space data on more than one volume is not yet supported.
