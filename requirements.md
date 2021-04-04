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
> The Spacemesh App is an Electron App. It is supported on any Linux distro that supports [Electron apps](https://electronjs.org/docs/tutorial/support).

## Operational Notes

### CPU Usage
As long as your system and configuration meets the recommended requirements, ongoing utilization of your CPU by the Spacemesh App should be limited during normal operation (after the initial setup phase) to 2 CPU cores.

### Network Configuration
Your network should allow the App to accept incoming connections on UDP port 7153 and on TCP port 7153 and your computer firewall should not block incoming UDP and TPC packets on this port. The App attempts to automatically configure your network using UPnP. In some cases you may need to configure your router and firewall manually. Follow [this guide](netconfig.md) to configure your network.

### Laptop Usage
You can install the App, run a Smesher and produce blocks on your laptop if it meets the minimum system requirements. However, you will need to make sure you leave your laptop open and connected to power and to the Internet 24/7.

Occasionally shutting down your laptop or the App may prevent you from Smeshing blocks and from earning Smeshing rewards.

---

## Spacemesh App Requirements - Spacemesh 0.2 - TweedleDum Open Testnet (Not yet released)

### Minimum System Requirements
- A computer with a modern Intel or AMD CPU (4 cores / 8 native threads) or an Apple M1 CPU.
- Operating System: Windows 10 (Home or Pro), macOS, Ubuntu 12.04, Fedora 21, or Debian 8.
- 8 GB RAM.
- 350 GB free space (HDD or SSD).
- A graphics card supporting CUDA compute API 9.0 or later, or Vulkan compute API 1.1 or later.
- An always-on, unmetered Internet connection capable of 5 mbps download and 1 mbps upload.

---

### Recommended System Requirements
- A desktop computer with modern Intel or AMD CPU (8 cores / 16 native threads).
- Operating System: Windows 10 (Home or Pro), macOS, Ubuntu 12.04, Fedora 21, or Debian 8.
- 16 GB RAM.
- 350GB free space (HDD or SSD).
- A discrete gaming graphics card supporting CUDA compute API 9.0 or later, or Vulkan compute API 1.1 or later. For example, an AMD Radeon RX card or an Nvidia Geforce RTX card.
- An always-on, unmetered Internet connection capable of 10 mbps download and 1 mbps upload.

### Recommended Free Disk Space
- The minimum proof of space data file size is 250 GiB.
- You can create a larger proof of space data files, e.g. 350 GiB, 450 GiB, 550 GiB, etc... as long as you have sufficient free disk space on one of your hard drives.
- You can use any magnetic hard drive (HDD) or SSD drive for the proof of space data.
- There is no significant advantage in using an SSD over HDD.
- You do not need to have temporary disk space larger than your final proof of space data.
- Creating a proof of space on more than one volume is not yet supported.
- You need sufficient disk space for your local Spacemesh p2p node data and for your proof of space data file. We recommend at least 300 GiB of free disk space in total. 250 GiB for the proof of space data file and 50 GiB for node data.

### Recommended Hardware for Proof of Space Data
We recommend creating the proof of space data using a discrete GPU card in a Desktop Computer such as AMD Radeon, Nvidia Geforce or Nvidia Tesla. You can also create the proof of space data using your computer's integrated graphics card or main CPU. However, it will take much longer to generate the data, and the process is less energy efficient so we do not recommend it.

#### Supported Discrete GPUs
The following popular GPU models are supported.

- Nvidia Geforce RTX 2070 / 2080
- Nvidia GTX 1060
- AMD Radeon RX 570 / 580
- AMD Radeon Pro 555x
- Nvidia Tesla V100, T4, P100 or P4

Other Nvidia discrete cards should work if they support `CUDA compute API 9.0 or later`.

Other AMD discrete cards should work if they support `Vulkan API 1.1 or later`.

#### Integrated GPUs
The following popular integrated GPUs models are supported but are not recommended due to their slow performance compared to discrete GPUs.
- Apple M1
- Intel UHD Graphics 630

#### Performance
The time it takes to create the proof of space data depends on your GPU compute capabilities. Entry-level discrete GPUs have slower compute performance compared to high-end ones, and much faster performance than integrated GPUs.
