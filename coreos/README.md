# CoreOS Setup
Install CoreOS on Intel NUC

## Get Ready
using my mac

*NOTE* iPXE did not work on my NUC5CPYH

- Get CoreOS iso
- Burn it to a USB flashdrive `sudo dd if=coreos_production_iso_image.iso of=/dev/disk2 bs=4m && sync`
- Create cloud-config.yml and push to github

## Install CoreOS
- Boot NUC from USB flashdrive
- Get cloud-config.yml `wget https://raw.githubusercontent.com/<URL_TO>/cloud-config.yml`
- Install CoreOS to SDD `sudo coreos-install -d /dev/sda -C stable -c cloud-config.yml`
