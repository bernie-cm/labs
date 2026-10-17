## Installing Proxmox VE
Proxmox VE (Virtual Environment) is an open-source server management platform that allows you to run multiple VMs. I picked it because I was running Fedora on an old 32GB RAM desktop machine, and I wanted to make that old computer a part of my homelab cluster.
### Installation process
1. Download the ISO and flash a USB drive

How to check the download with the SHA sum, to confirm that the downloaded ISO isn’t corrupted or hasn’t been altered. The SHA256 hash is like a fingerprint, and Proxmox publishes the “fingerprint” of the real file.

The current hash of Proxmox VE 9.2 is
SHA256SUM
4e88fe416df9b527624a175f24c9aa07c714d3332afb1ee3dbf3879573ef2c6c

And that matches the hash of the file I have
```
$ shasum -a 256 proxmox-ve_9.2-1.iso
4e88fe416df9b527624a175f24c9aa07c714d3332afb1ee3dbf3879573ef2c6c  proxmox-ve_9.2-1.iso
$
```
