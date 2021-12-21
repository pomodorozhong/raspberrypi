# Headless setup for wifi

Reference: [Headless Raspberry Pi 4 SSH WiFi Setup (Mac + Windows, 10 Steps) – desertbot.io](https://web.archive.org/web/20211221043445/https://desertbot.io/blog/headless-raspberry-pi-4-ssh-wifi-setup)

## Instruction

Create a file in the root of `boot` called: `wpa_supplicant.conf`. Then paste the following into it (adjusting for your [ISO 3166 alpha-2 country code](https://en.wikipedia.org/wiki/List_of_ISO_3166_country_codes), network name and network password):

```
country=TW
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1

network={
    ssid="NETWORK-NAME"
    psk="NETWORK-PASSWORD"
}
```