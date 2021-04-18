## Spacemesh App Requirements - Spacemesh 0.1 Release

### Minimum System Requirements

- A computer with modern Intel or AMD CPU (3 cores / 6 native threads).
- OS: Windows 10 (Home or Pro), macOS, Ubuntu 18.04, Fedora 21, or Debian 8.
- 6 GB RAM.
- 150 GB free space. (HDD or SSD).
- An always-on, unmetered Internet connection capable of 5 mbps download and 1 mbps upload.

---

### Recommended System Requirements

- A desktop computer with modern Intel or AMD CPU (4 cores / 8 native threads or better).
- OS: Windows 10 (Home or Pro), macOS, Ubuntu 20.04, Fedora 21, or Debian 8.
- 8 GB RAM.
- 350GB free space. (HDD or SSD).
- An always-on, unmetered Internet connection capable of 10 mbps download and 1 mbps upload.

### Linux Systems
> The Spacemesh App is an Electron App. It is supported on any Linux distribution that supports [Electron apps](https://electronjs.org/docs/tutorial/support).

## Operational Notes

### CPU Usage
As long as your system and configuration meets the recommended requirements, ongoing utilization of your CPU by the Spacemesh App should be limited during normal operation (after the initial setup phase) to 2 CPU cores.

### Network Configuration
Your network should allow the App to accept incoming connections on UDP port 7153 and on TCP port 7153 and your computer firewall should not block incoming UDP and TPC packets on this port. The App attempts to automatically configure your network using UPnP. In some cases you may need to configure your router and firewall manually. Follow [this guide](netconfig.md) to configure your network.

### Laptop Usage
You can install the App, run a Smesher and produce blocks on your laptop if it meets the minimum system requirements. However, you will need to make sure you leave your laptop open and connected to power and to the Internet 24/7.

Occasionally shutting down your laptop or the App may prevent you from Smeshing blocks and from earning Smeshing rewards.

---

## System Requirements - Spacemesh 0.2 - TweedleDum Open Testnet (Not yet released)

> Note that all the information below is tentative, and is subject to change around Spacemesh 0.2 testnet launch date.

### Spacemesh App

Following are the system requirements for running the Spacemesh App (Smapp) and to smesh using a full Spacemesh p2p node managed by Smapp.

> We recommend this setup for users who are comfortable using desktop apps but are not comfortable using the command line.

With this setup, you should be able to use your computer normally for other interactive apps.

- A desktop computer with a modern Intel, AMD or Apple M1 CPU (4 cores / 8 native threads).
- Windows 10 Home or Pro, macOS, Ubuntu 18.04 (or later), Fedora 21 (or later), or Debian 8 (or later).
- 8 GB RAM minimum. 16 GB RAM recommended.
- 300 GiB free disk space (HDD or SSD).
- A discrete graphics card supporting CUDA compute API 9.0 or later, or Vulkan compute API 1.1 or later. For example, AMD Radeon RX or Nvidia Geforce RTX. The graphics card is used to setup proof of space time data which is required for smeshing.
- An always-on, unmetered Internet connection capable of 10 mbps download and 1 mbps upload.

The following popular models are examples for computers with these requirements:

- [Apple Mac Mini](https://www.apple.com/shop/buy-mac/mac-mini/apple-m1-chip-with-8-core-cpu-and-8-core-gpu-256gb)
- [HP Pavillion Gaming Desktop PC TG01](https://www.amazon.com/HP-Pavilion-i3-10100-Keyboard-TG01-1022/dp/B08NCFRFFD)
- [HP Pavillion Gaming Desktop PC TP01](https://www.amazon.com/HP-Business-Processor-i9-10850K-Bluetooth/dp/B08257GC1Q)

----

### Spacemesh Full Node

Following are the requirements for running the a Spacemesh full node, and to smesh without running the Spacemesh App.

> We recommend this setup to technical users who are comfortable with the command line.

With this setup, your computer will be dedicated to running the Spacemesh full node and will not be used for running other interactive apps.

- A computer with a modern Intel, an AMD CPU (2 cores / 4 native threads) or an Apple M1 CPU.
- Windows 10 Home or Pro, macOS, Ubuntu 18.04, Fedora 21, or Debian 8.
- 4 GB RAM.
- 300 GiB free disk space (HDD or SSD).
- A graphics card supporting CUDA compute API 9.0 or later, or Vulkan compute API 1.1 or later is recommended to setup proof of space data which is needed for smeshing (see below).
- An always-on, unmetered Internet connection capable of 10 mbps download and 1 mbps upload.

---

### About Proof of Space Data

You only need to setup proof of space data once to smesh for an unlimited period of time. The minimum proof of space data size is 200 GiB.

You can create larger proof of space data up to the maximum size in 50 GiB increments from the minimum size. For example, 250 GiB, 300 GiB, 350 GiB, etc... up to the free space in a one volume on one or more of your drives.

> The larger your proof of space data is, the higher your smeshing rewards will be.

The maximum proof of space data size has not been finalized yet but is likely to be around 1 PiB.

You can use any magnetic hard drive (HDD) or SSD drive for storing proof of space data. There is no significant advantage in using an SSD over HDD.

You do not need to have temporary disk space larger than your final proof of space data.

Creating proof of space data on more than one volume is not yet supported.

> You need to have sufficient disk space for your Spacemesh full node data and for your proof of space data. We recommend at least 300 GiB of free disk space in total. 256 GiB for the proof of space data, and 50 GiB for the node's data.

### Recommended Hardware for Proof of Space Data Creation
We recommend creating proof of space data using a discrete GPU such as AMD Radeon, Nvidia GeForce or Nvidia Tesla.

> You can also create the proof of space data using your computer's integrated graphics card or its main CPU. However, it will take much longer, and the process will be less energy efficient so we do not recommend it.

The following popular discrete GPU models are supported.

- Nvidia Geforce RTX 2070 / 2080.
- Nvidia GTX 1060.
- AMD Radeon RX [550](https://www.newegg.com/onda-model-rx550-4g/p/1DW-00C1-00001) / 570 / 580.
- AMD Radeon Pro 555x.
- Nvidia Tesla V100, T4, P100 or P4.

> Other Nvidia models should work if they support `CUDA compute API 9.0 or later`. Other AMD models should work if they support `Vulkan API 1.1 or later`.

The following popular integrated GPUs models are supported but are not recommended due to their slow performance compared to discrete GPUs.

- Apple M1
- Intel UHD Graphics 630

#### Performance
The time it takes to create proof of space data depends on your GPU compute capabilities and the specified data size. Entry-level discrete cards have slower compute capabilities compared to high-end ones, and much better compute performance than integrated GPUs.

Below are rough estimated times for creating a 250 GiB proof of space data using various popular gpus and cpus models:
- Nvidia RTX 2070: 10 hours.
- AMD Radeon RX 580: 20 hours.
- AMD Radeon Pro 560x: 40 hours.
- Apple M1: 50 hours.
- AMD/Intel modern CPU (~3.8 ghz), 8 native threads: 185 hours.
