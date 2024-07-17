
# openwrt-xray

Xray installations in OpenWRT for routers with small memory

## Tested device

Xiaomi 4C
## Clone repo

```
git clone https://github.com/tim06/openwrt-xray.git
```

## Installing the prepared OpenWRT firmware 

// screenshot

## Copying materials to the router

```
cd openwrt-xray
scp geoip.dat geosite.dat root@192.168.1.1:/ush/share/xray
scp xray-core_1.6.4-1_mipsel_24kc.ipk luci-app-xray_3.4.1-r1_all.ipk luci-app-xray-status_3.4.1-r1_all.ipk root@192.168.1.1:/tmp/
```
## Install xray

```
ssh root@192.168.1.1
cd /tmp/
opkg install xray-core_1.6.4-1_mipsel_24kc.ipk
```
## Clearing the installation file

```
rm xray-core_1.6.4-1_mipsel_24kc.ipk
```

## Install ui luci-xray

```
opkg install *
```
## Reboot
```
reboot
```
After rebooting, a new Services -> Xray tab will appear in the OpenWRT ui-panel with the ability to configure the connection.
