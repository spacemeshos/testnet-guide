# Installer Verification

Follow the steps below to verify the integrity and authenticity of the Spacemesh downloadable installer for your platform.

### OS X

COMING SOON

1. Open Terminal and run `shasum` on the downloadable installer:

```bash
shasum -a 512 /path/to/installer
```

2. Verify that the shasum output you got in terminal matches this checksum:

<script>console.log('test script in .md file')</script>

<span>
dmg_sha512
</span>

### Windows 10

COMING SOON

1. Run `certutil` from the Windows command line console:

```shell
certutil -hashfile C:\path\to\installer SHA512
```

2. Verify that the output you got in the console matches this checksum:

<span>
exe_sha512
</span>

### Debian

COMING SOON

1. Run `sha512sum` from the command line:

```bash
sha512sum \path\to\downloaded\installer
```

2. Verify that the output you got in the console matches this checksum:

<span>
deb_sha512
</span>

### Ubuntu or Fedora Linux

COMING SOON

1. Run `sha512sum` from the command line:

```bash
sha512sum \path\to\downloaded\installer
```

2. Verify that the output you got in the console matches this checksum:

<span>
AppImage_sha512
</span>
