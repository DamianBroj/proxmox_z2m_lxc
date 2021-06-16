# NOT WORKING

# Proxmox Zigbee2MQTT LXC Container
(curl. sudo, auto login)

To create a new Proxmox Zigbee2MQTT LXC Container, run the following steps.

STEP #1 (Run in the Proxmox web shell)
```
bash -c "$(wget -qLO - https://github.com/tteck/proxmox_z2m_lxc/raw/master/create_container.sh)"
```
You must update the list of devices (ports) that are shared with the LXC ID of 100 (change to your ID), run the following in the Proxmox web shell.

STEP #2 (Run in the Proxmox web shell)
```
bash -c "$(wget -qLO - https://github.com/whiskerz007/proxmox_hassio_lxc/raw/master/set_autodev_hook.sh)" -s 100
```
Note: The changes will apply on the next start of the LXC.

STEP #3 Determine the location of your adapter (Run in the zigbee2mqtt console)
```
ls -l /dev/serial/by-id
```
Next follow the instructions from the link below to complete the setup

STEP #3 ( Run in your browser)
```
https://www.zigbee2mqtt.io/getting_started/running_zigbee2mqtt.html#3-configuring
```

