# esphome-configs


```yaml
substitutions:
    name: bt-proxy # add mac address suffix to prevent duplicate hostnames
    # friendly_name: Bluetooth Proxy

packages:
    azndibs.btproxy: github://AznDibs/esphome_configs/bt-proxy.yaml@main

esphome:
    name_add_mac_suffix: false

api:
    encryption:
        key: !secret api_key
ota:
    password: !secret ota_password

wifi:
    ssid: !secret wifi_ssid
    password: !secret wifi_password
    ap:
        password: !secret ap_password
```

In your esphome config.yaml:
```yaml
    api_key: # your own key
    ota_password: # your own ota password
    
    wifi_ssid: # your own ssid
    wifi_password: # your own wifi password

    ap_password: # your own ap password
```