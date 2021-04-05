## Spacemesh App Requirements - Spacemesh 0.1 Release

### Minimum System Requirements

- A computer with modern Intel or AMD CPU (3 cores / 6 native threads).
- OS: Windows 10 (Home or Pro), macOS, Ubuntu 12.04, Fedora 21, or Debian 8.
- 6 GB RAM.
- 150 GB free space. (HDD or SSD).
- An always-on, unmetered Internet connection capable of 5 mbps download and 1 mbps upload.

---

### Recommended System Requirements

- A desktop computer with modern Intel or AMD CPU (4 cores / 8 native threads or better).
- OS: Windows 10 (Home or Pro), macOS, Ubuntu 12.04, Fedora 21, or Debian 8.
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


### Spacemesh App

> These are the requirements for running the Spacemesh App (Smapp) and to smesh using a full p2p node managed by Smapp. You should be able to use the computer normally for other interactie apps. We recommend this setup for users who are comfortable using desktop apps but who are not comfortable using command line apps.

- A desktop computer with a modern Intel, AMD or Apple M1 CPU (4 cores / 8 native threads).
- Operating System: Windows 10 (Home or Pro), macOS, Ubuntu 18.04 (or later), Fedora 21 (or later), or Debian 8 (or later).
- Minimum 8 GB RAM. 16 GB RAM is recommended.
- At least 300 GiB free disk space (HDD or SSD).
- A discrete gaming graphics card supporting CUDA compute API 9.0 or later, or Vulkan compute API 1.1 or later. For example, an AMD Radeon RX card or an Nvidia Geforce RTX card. The graphics card is used to setup proof of space time data which is required for smeshing.
- An always-on, unmetered Internet connection capable of 10 mbps download and 1 mbps upload.

The following popular desktop computer models meet these requirements:

- [Apple Mac Mini](https://www.apple.com/shop/buy-mac/mac-mini/apple-m1-chip-with-8-core-cpu-and-8-core-gpu-256gb)
- [HP Pavillion Gaming Desktop PC TG01](https://www.amazon.com/HP-Pavilion-i3-10100-Keyboard-TG01-1022/dp/B08NCFRFFD)
- [HP Pavillion Gaming Desktop PC TP01](https://www.amazon.com/HP-Business-Processor-i9-10850K-Bluetooth/dp/B08257GC1Q)

----

### Spacemesh Full p2p Node

These are the requirements for runinh the a full Spacemesh p2p node and to smesh without running the Spacemesh App.

>We recommend this methods for technical users who are comfortable with the command line and with working with terminal apps.

In this setup, the computer will be dedicated to run the node and will not able to support interactive use of other apps.

- A computer with a modern Intel or AMD CPU (2 cores / 4 native threads) or an Apple M1 CPU.
- Operating System: Windows 10 (Home or Pro), macOS, Ubuntu 12.04, Fedora 21, or Debian 8.
- 4 GB RAM.
- At least 300 GiB free disk space (HDD or SSD).
- A graphics card supporting CUDA compute API 9.0 or later, or Vulkan compute API 1.1 or later is needed to setup proof of space time data which is required for smeshing.
- An always-on, unmetered Internet connection capable of 10 mbps download and 1 mbps upload.

---

### About Proof of Space Data

You only need to setup proof of space data once to smesh for an unlimited period of time. The minimum proof of space data size is 250 GiB.

You can create larger proof of space data , e.g. 350 GiB, 450 GiB, 550 GiB, etc... as long as you have sufficient free disk space on one of your hard drives.

> The larger your proof of space data is, the higher your smeshing rewards will be.

The maximum proof of space data size has not been finalized yet but is likely to be 250 TiB.

You can use any magnetic hard drive (HDD) or SSD drive for the proof of space data. There is no significant advantage in using an SSD over HDD.

You do not need to have temporary disk space larger than your final proof of space data.

Creating a proof of space on more than one volume is not supported.

> You need to have sufficient disk space for your Spacemesh p2p full node data and for your proof of space data. We recommend at least 300 GiB of free disk space in total. 250 GiB for the proof of space data and 50 GiB for the node's local data.

### Recommended Hardware for Proof of Space Data Creation
We recommend creating the proof of space data using a discrete GPU card such as AMD Radeon, Nvidia Geforce or Nvidia Tesla.

> You can also create the proof of space data using your computer's integrated graphics card or the main CPU. However, it will take much longer to create the data, and the process is less energy efficient so we do not recommend it.

#### Discrete GPUs
The following popular GPU models are supported.

- Nvidia Geforce RTX 2070 / 2080
- Nvidia GTX 1060
- AMD Radeon RX [550](https://www.newegg.com/onda-model-rx550-4g/p/1DW-00C1-00001) / 570 / 580
- AMD Radeon Pro 555x
- Nvidia Tesla V100, T4, P100 or P4

> Other Nvidia discrete cards should work if they support `CUDA compute API 9.0 or later`. Other AMD discrete cards should work if they support `Vulkan API 1.1 or later`.

#### Integrated GPUs
The following popular integrated GPUs models are supported but are not recommended due to their slow performance compared to discrete GPUs.
- Apple M1
- Intel UHD Graphics 630

#### Performance
The time it takes to create the proof of space data depends on your GPU compute capabilities and the data size.

Entry-level discrete GPUs have slower compute performance compared to high-end ones, and much faster performance than integrated GPUs.
