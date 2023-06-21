## Sentinel AI Drone Wifi Setup for Drexel's (dragonfly network)

To use the wifi I had to create a wifi conf file as given below. Use the configuration given at the Drexel Wifi - https://drexel.edu/it/help/a-z/dragonfly3/generic_config/

path to the file need to be edited: `/data/misc/wifi/wpa_supplicant.conf`

```
ctrl_interface=DIR=/data/misc/wifi/wpa_supplicant GROUP=wifi
update_config=1
device_name=voxl
manufacturer=ModalAI
model_name=voxl
model_number=1.0

network={
    ssid="dragonfly3"
    key_mgmt=WPA-EAP
    eap=PEAP
    identity="Drexel_User_ID"
    password="Drexel_Password"
    phase1="peaplabel=0"
    phase2="auth=MSCHAPV2"
}

```

and now just reboot via `sudo reboot`
