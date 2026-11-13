# Welcome to MINUX!

> MINUX is a minimalist Arch Linux-based distribution.<br/>
> In fact, it is a customized ISO for my personal environment.
> This is the arch based linux for ML environment.

# Download

Download the ISO and `SHA256SUMS` from the [latest release](https://github.com/kuper0201/minux_ml_iso/releases/latest). No GitHub login is required.

Successful builds on `main`, the weekly schedule, and manual workflow runs automatically publish a new release and mark it as Latest. Release tags include the build date, workflow run number, and attempt so previous builds remain available.

To verify the downloaded ISO, place it beside `SHA256SUMS` and run:

```sh
sha256sum -c SHA256SUMS
```

# Installation

Boot the ISO in UEFI mode, connect to the network (`nmtui` if needed), then run `setup-minux` as root. Select your target disk and user settings in Archinstall. MINUX customization runs inside Archinstall before its final reboot prompt; a failed customization stops the installation.

The ISO pins the installation scripts and desktop configuration to tested commits. Installation needs access to the Arch mirrors, GitHub, and AUR. The customization log is saved to `/var/log/minux-install.log` on the installed system, and `/var/lib/minux/install-complete` records the scripts commit only after successful completion.

For an existing Archinstall JSON configuration, use `setup-minux --config /path/to/config.json`; other Archinstall options are forwarded.

# Packages
```text
linux-lts
yay
openbox
nvidia-dkms
lightdm
micrimamba
docker
```

RealVNC is installed but starts only after licensing is configured. Then run `sudo systemctl enable --now vncserver-x11-serviced` to enable remote access. This prevents the unlicensed status window from covering the login screen.
