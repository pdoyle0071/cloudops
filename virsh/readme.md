# Virsh

This repository contains configuration files for managing Ubuntu VMs with `virsh` and `cloud-init`.


## Notes

- `user-data.yml` is sanitized (no passwords or SSH keys). Replace placeholders with your secrets before use.
- All VMs are intended to use the `br0` bridge on the host.
- Use `virsh` or `virt-install` commands in `virsh.txt` to deploy VMs.

## How to use

1. Copy `user-data.yml` and fill in:
   - `username`
   - `password` (hashed)
   - `ssh-authorized-keys`
2. Create the VM with `virsh` using the commands in `virsh.txt`.
3. Adjust MAC addresses or disk paths if needed for your host environment.


This will create a ubunbtu 22.04 server with the elements as outlined in the cloud-init file as an automated install

	
