# GlobesurferX.1
This is it USBIP Server for router Option Globesurfer X.1
see howto.txt

Installation ( After your router running openwrt )
1. Ssh to the router
2. opkg update
3. opkg install usbip usbip-server kmod-usbip-host
4. (optional) opkg install kmod-usb-core kmod-usb2 kmod-usb3
  # Load the modules
6. modbprobe usbip-core
7. modprobe usbip-host

# If you're seeing -ash: usbip: not found, it means the usbip tools are not installed or not available for your OpenWrt build.

Fixes :
1. ssh to the router
2. opkg update
3. opkg list | grep usbip
    - you will see something like this
    - usbip - 2.0-1 - USB/IP utilities
    - usbip-server - ...
    - usbip-client - ...
    - kmod-usbip-host - ...
    - kmod-usbip-vhci - ...
4. opkg install usbip usbip-server kmod-usbip-host
