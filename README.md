# Proxmox LXC Container


To create a new Proxmox LXC container, run the following in the Proxmox web shell.

```
bash -c "$(wget -qLO - https://github.com/tteck/proxmox_create_lxc_plus/raw/master/create_container.sh)"
```
To update the list of devices (ports) that are shared with the LXC ID of 100 (change to your ID), run the following in the Proxmox web shell.

```
bash -c "$(wget -qLO - https://github.com/whiskerz007/proxmox_hassio_lxc/raw/master/set_autodev_hook.sh)" -s 100
```
Note: The changes will apply on the next start of the LXC.

Ports can be tested by executing: test -w [PORT] && echo success || echo failure

Example:
```
test -w /dev/ttyACM0 && echo success || echo failure
```
