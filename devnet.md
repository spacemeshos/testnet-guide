# Spacemesh 0.2 Preview Release

Latest release: v0.2.0-rc7 (Network Id 203)

> This early Spacemesh 0.2 technical preview release is intended for users who are comfortable with using the command line and terminal applications.

Follow these instructions to join the Spacemesh 0.2 devnet.

## Minimum System Requirements

- A computer with a modern Intel or AMD x86-64 CPU with at least 2 cores / 4 native threads or an Apple M1 CPU.
- Windows 10 Home or Pro, macOS or Ubuntu 20.04. Other modern Linux distributions should also work.
- 4 GB RAM.
- 100 GiB free disk space (HDD or SSD).
- An always-on, unmetered Internet connection with at least 10 mbps download and 1 mbps upload speed.

## Recommended System Requirements
- 8 GB RAM.
- An Nvidia GPU and driver with CUDA support (minimum compute compatibility 5.0, maximum compute compatibility 8.6) such as Nvidia driver version R450 or newer.
- A GPU with Vulkan 1.2 support such as a modern AMD GPU, Apple M1 CPU/GPU, or Intel GPU.

## Installing and Running

1. Download the devnet release zip file for your platform

- [Windows](https://github.com/spacemeshos/go-spacemesh/releases/download/v0.2.0-rc7/windows.zip)
- [macOS](https://github.com/spacemeshos/go-spacemesh/releases/download/v0.2.0-rc7/macOS.zip)
- [Linux](https://github.com/spacemeshos/go-spacemesh/releases/download/v0.2.0-rc7/linux.zip)

2. Extract the zip file to a directory and navigate to it in terminal

3. Configure downloaded binaries

#### Linux and macOS
Set binaries execution permissions.

```bash
chmod u+x go-spacemesh
chmod u+x lib*
chmod u+x smrepl
```

#### macOS
Enable downloaded binaries execution.

```bash
sudo xattr -rd com.apple.quarantine go-spacemesh
sudo xattr -rd com.apple.quarantine lib*
sudo xattr -rd com.apple.quarantine smrepl
```

Or alternatively try

```bash
spctl --add go-spacemesh
spctl --add lib*
spctl --add smrepl
```

4. Start a Spacemesh full node

#### macOS and Linux
```bash
./go-spacemesh -c config.json > log.txt
```

#### Windows (PowerShell)

```PowerShell
.\go-spacemesh.exe -c config.json > log.txt
```

5. Start Smrepl

Open another terminal window or tab.

> Due to a known issue please wait for up to 45 seconds from the time you start the go-spacemesh node in the previous step before starting smrepl.

#### macOS and Linux

```bash
./smrepl
```

#### Windows (PowerShell)

```PowerShell
.\smrepl_windows_amd64.exe
```

Proceed to create a wallet and setup smeshing in smrepl.

----

### Using the gpu-post test app
Navigate to your directory you extract the zip release to and enter from a terminal:

#### macOS
```bash
export DYLD_LIBRARY_PATH=.:$DYLD_LIBRARY_PATH
chmod +x gpu-setup-test
./gpu-setup-test
```

#### Linux
```bash
export LD_LIBRARY_PATH=.:$LD_LIBRARY_PATH
chmod +x gpu-setup-test
./gpu-setup-test
```

#### Windows (PowerShell)
```PowerShell
.\gpu-setup-test.exe
```

---

## Building from Source Code

> You can join the devnet by building this release binaries from source code from our public github repos instead of using our provided binaries.

1. Clone and build go-spacemesh [from this tag](https://github.com/spacemeshos/go-spacemesh/tree/v0.2.0-rc7)

2. Clone and build smrepl [from this tag](https://github.com/spacemeshos/smrepl/tree/v0.1.32)

3. Clone and build gpu-post [from this tag](https://github.com/spacemeshos/gpu-post/tree/v0.1.22)

4. Copy the gpu-post artifacts for your platform to your go-spacemesh directory.

5. Run the full node with this devnet [config file](https://github.com/spacemeshos/go-spacemesh/releases/download/v0.2.0-rc7/config.json)

---

## Devnet 0.2 Mini Technical FAQ
Q: My node stopped syncing. I waited a long time but the current layer doesn't advance. What should I do?

A: Stop the node process by preccing `ctrl-c` in the terminal window you started the node at. Delete local node data folder `~/spacemesh/<devnet_id>/` and proof of spacetime data from your post directory if you created any, and start it again.

---

Q: I've setup smeshing via smrepl and I had later restart the node and now it is not smeshing. How can I keep smeshing after a node restart?

A: After setting post in smrepl, you need to modify your node's config file with the smeshing parameters so your node can continute smeshing using these parameters after you restart it.
