![GitHub Downloads (all assets, all releases)](https://img.shields.io/github/downloads/gaofengnan/zls-debian/total)
![GitHub Downloads (all assets, latest release)](https://img.shields.io/github/downloads/gaofengnan/zls-debian/latest/total)
![GitHub Release](https://img.shields.io/github/v/release/gaofengnan/zls-debian)
![GitHub Release Date](https://img.shields.io/github/release-date/gaofengnan/zls-debian)

<h1>
   <p align="center">
     <a href="https://github.com/zigtools/zls/"><img src="https://github.com/gaofengnan/zls-debian/blob/main/zls-logo.png" alt="Zls Logo" width="128" style="margin-right: 20px"></a>
     <a href="https://www.debian.org/"><img src="https://github.com/gaofengnan/zls-debian/blob/main/debian-logo.png" alt="Debian Logo" width="104" style="margin-left: 20px"></a>
     <br>ZLS for Debian
   </p>
</h1>
<p align="center">
 ZLS is a non-official implementation of the Language Server Protocol for Zig in Zig. It provides developers with IDE features in their editor.
</p>

# Zls for Debian

> Fork of [dariogriffo/zls-debian](https://github.com/dariogriffo/zls-debian) (MIT); the original packaging is by Dario Griffo. Served at [deb.gaofn.xyz](https://deb.gaofn.xyz) for Debian 12 (bookworm) and 13 (trixie).

This repository contains build scripts to produce the _unofficial_ Debian packages
(.deb) for [Zls](https://github.com/zigtools/zls) hosted at [deb.gaofn.xyz](https://deb.gaofn.xyz)

Currently supported Debian distros are:
- Bookworm (v12)
- Trixie (v13)
- Forky (v14)
- Sid (testing)

Currently supported Ubuntu distros are:
- Jammy (22.04)
- Noble (24.04)
- Questing (25.10)
- Resolute (26.04)

Supported architectures:
- amd64 (x86_64)
- arm64 (aarch64)
- armhf (32-bit ARM, hard float)
- i386 (x86 32-bit)
- ppc64el (POWER little-endian)
- riscv64
- s390x
- loong64 (LoongArch64)

Every zls binary is statically linked, so each package runs on every suite it
is built for and needs no dependencies.

This is an unofficial community project to provide a package that's easy to
install on Debian. If you're looking for the Zls source code, see
[zigtools/zls](https://github.com/zigtools/zls).

## Install/Update

### The Debian way

```sh
sudo install -d -m 0755 /etc/apt/keyrings
sudo curl -fsSL https://deb.gaofn.xyz/deb.gaofn.xyz.gpg -o /etc/apt/keyrings/deb.gaofn.xyz.gpg
sudo curl -fsSL https://deb.gaofn.xyz/deb.gaofn.xyz.sources -o /etc/apt/sources.list.d/deb.gaofn.xyz.sources
# Debian 12 (bookworm): fetch deb.gaofn.xyz-bookworm.sources instead
sudo apt update
sudo apt install zls
```

### Manual Installation

1. Download the .deb package for your Debian version available on
   the [Releases](https://github.com/gaofengnan/zls-debian/releases) page.
2. Install the downloaded .deb package.

```sh
sudo dpkg -i <filename>.deb
```
## Updating

To update to a new version, just follow any of the installation methods above. There's no need to uninstall the old version; it will be updated correctly.

## Contributing

I want to have an easy-to-install Zls package for Debian, so I'm doing what
I can to make it happen.
If you want to test locally, you should be able to run
[build_zls_debian.sh](https://github.com/gaofengnan/zls-debian/blob/main/build_zls_debian.sh)
on your own Debian system, only requirement is docker.

## Roadmap

- [x] Produce a .deb package on GitHub Releases
- [x] Set up a debian mirror for easier updates

## Disclaimer

- This repo is not open for issues related to zls. This repo is only for _unofficial_ Debian packaging.
- This repository is based on the amazing work of [Mike Kasberg](https://github.com/mkasberg) and his [Zig Ubuntu](https://github.com/mkasberg/ghostty-ubuntu) packages
