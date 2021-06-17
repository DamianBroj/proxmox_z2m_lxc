# Proxmox Zigbee2MQTT LXC Container

To create a new Proxmox Zigbee2MQTT LXC Container, run the following steps.

STEP #1 (Run in the Proxmox web shell)
```
bash -c "$(wget -qLO - https://github.com/tteck/proxmox_z2m_lxc/raw/master/create_container.sh)"
```
You must update the list of devices (ports) that are shared with the LXC ID of 100 (change to your ID), run the following in the Proxmox web shell.

STEP #2 (Run in the Proxmox web shell)
```
bash -c "$(wget -qLO - https://github.com/tteck/proxmox_z2m_lxc/raw/master/open_port.sh)" -s 100
```
## Note: Restart the zigbee2mqtt LXC to apply changes before continuing.

STEP #3 Determine the location of your adapter (Run in the zigbee2mqtt console)
```
ls -l /dev/serial/by-id
```
Example Output: ```/dev/serial/by-id/usb-1a86_USB_Serial-if00-port0```

Next follow the instructions from the link below to complete the setup

STEP #4 ( Run in your browser)
```
https://www.zigbee2mqtt.io/getting_started/running_zigbee2mqtt.html#3-configuring
```

First 9 lines in my zigbee2mqtt config
```
frontend:
  port: 9442
homeassistant: true
permit_join: false
mqtt:
  base_topic: zigbee2mqtt
  server: 'mqtt://192.168.86.224:1883'
  user: <usr>
  password: <pwd>
  ```
  
