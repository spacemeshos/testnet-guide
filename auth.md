# Verifying the Downloadable Installer

Follow the steps to verify the integrity and authenticity of the Spacemesh downloadable installer for your platform.

### OS X
[SPACEMESH_OS_X_INSTALLER](https://s3.amazonaws.com/app-binaries.spacemesh.io/Spacemesh+Wallet-0.0.1.dmg)

1. Open Terminal and run `shasum` on the downloadable installer:

```bash
shasum -a 512 /path/to/installer
```

2. Verify that the shasum output you got in terminal matches this checksum:

<span>
9e59d0f84fd3bb42537d782beced001b35235d840da4657761f8bc74d599bb5432661a74faccd1ab6b814716ff37c8a6977e8b508e6972861b75bf61c79a565a
</span>

### Windows 10
[SPACEMESH_WIN10_INSTALLER](https://s3.amazonaws.com/app-binaries.spacemesh.io/Spacemesh+Wallet+Setup+0.0.1.exe)

1. Run `certutil` from the Windows command line console:
```shell
certutil -hashfile C:\path\to\installer SHA512
```

2. Verify that the output you got in the console matches this checksum:

<span>
312b3cfeec4653020b646dae79f172470a9900203b73a21b03d08cba4eb5ee3f342a2efb37c24497d796eea9fca2376b74f2946622102233bfc8909e5b261f76
</span>

### Debian

[SPACEMESH_DEB_INSTALLER](https://s3.amazonaws.com/app-binaries.spacemesh.io/smapp_0.0.1_amd64.deb)

1. Run `sha512sum` from the command line:

```bash
sha512sum \path\to\downloaded\installer
```

2. Verify that the output you got in the console matches this checksum:

<span>
4c6b8963c528ffd71264ec410163658e52d72667a2779c00fb4fd291cc8e7ab9a55a8177dd6805e250f1d70a661a28cde74290c654a23774301eec0a1cec5270
</span>

### Ubuntu or Fedora Linux

[SPACEMESH_UBUNTU_INSTALLER](https://s3.amazonaws.com/app-binaries.spacemesh.io/Spacemesh+Wallet+0.0.1.AppImage)

1. Run `sha512sum` from the command line:

```bash
sha512sum \path\to\downloaded\installer
```

2. Verify that the output you got in the console matches this checksum:

<span>
fa413d0651dd1accb9632bb82edc132c69640d14444bd5ce3bf629c6e6cbb0bb28fcf5c94b9ef287568548fb0403311fb72f6a6f8db8804997af7ae727c48712
</span>
