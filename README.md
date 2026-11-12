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
