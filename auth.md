# Verifying the Downloadable Installer

Follow the steps to verify the integrity and authenticity of the Spacemesh downloadable installer for your platform.

### OS X
[SPACEMESH_OS_X_INSTALLER](setup.app)

1. Open Terminal and run shasum on the downloadable installer:

```bash
shasum -a 256 /path/to/installer
```

2. Verify that the shasum output you got in terminal matches this checksum:

<span>
1b6d41e893868aab9e06e78a9902b925227c82d8e31978ff2c412c18ac99f49f70354715441385e0b96e4bd3e861d18fb30433d52e12b15b501fa790f36d0ea0
</span>

### Windows 10
[SPACEMESH_WIN10_INSTALLER](setup.app)

**SHA512 checksum**
1b6d41e893868aab9e06e78a9902b925227c82d8e31978ff2c412c18ac99f49f7035471544 1385e0b96e4bd3e861d18fb30433d52e12b15b501fa790f36d0ea0

1. Run `certutil` from the Windows command line console:
```shell
certutil -hashfile C:\path\to\installer SHA512
```

2. Verify that the output you got in the console matches this checksum:

<span>
1b6d41e893868aab9e06e78a9902b925227c82d8e31978ff2c412c18ac99f49f70354715441385e0b96e4bd3e861d18fb30433d52e12b15b501fa790f36d0ea0
</span>

### Debian

[SPACEMESH_DEB_INSTALLER](setup.deb)

1. Run `sha512sum` from the command line:

```bash
sha512sum \path\to\downloaded\installer
```

2. Verify that the output you got in the console matches this checksum:

<span>
1b6d41e893868aab9e06e78a9902b925227c82d8e31978ff2c412c18ac99f49f70354715441385e0b96e4bd3e861d18fb30433d52e12b15b501fa790f36d0ea0
</span>

### Ubuntu or Fedora Linux

[SPACEMESH_UBUNTU_INSTALLER](setup.pkg)

1. Run `sha512sum` from the command line:

```bash
sha512sum \path\to\downloaded\installer
```

2. Verify that the output you got in the console matches this checksum:

<span>
1b6d41e893868aab9e06e78a9902b925227c82d8e31978ff2c412c18ac99f49f70354715441385e0b96e4bd3e861d18fb30433d52e12b15b501fa790f36d0ea0
</span>
