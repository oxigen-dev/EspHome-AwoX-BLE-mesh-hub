# ESPHome component: AwoX BLE mesh (mqtt) hub

>
> **Supported devices/lights:**
> A list of supported devices can be found here => https://github.com/fsaris/EspHome-AwoX-BLE-mesh-hub/blob/main/components/awox_mesh/device_info.h#L90
>
> Devices not yet in this list will be recognized as a dimmable light. Create an issue with the `product id` (shown in model string of the mqtt discovery message/HomeAssistant device info) and the features of the device to get it added.
>

A ESPhome component (https://esphome.io/components/external_components.html#git) to create a MQTT hub for your AwoX BLE mesh devices.

For an example yaml see [`awox-ble-mesh-hub.yaml`](awox-ble-mesh-hub.yaml).

You will need your mesh credentials, easiest way to find them when comming from [AwoX MESH control component for Home Assistant](https://github.com/fsaris/home-assistant-awox) is to check the `/config/.storage/core.config_entries` file for `mesh_name` and `mesh_password`.

When setup the component will scan for AwoX BLE mesh devices and publish [discovery](https://www.home-assistant.io/integrations/mqtt/#mqtt-discovery) messages for each device on MQTT. When using HomeAssistant the device will show up under the MQTT integration. And you can (re)name the devices there.

In case of using a WLAN with hidden SSID, mind to use the multiple netowrk option, to define the hidden variable of the wifi network: [Connecting to Multiple Networks](https://esphome.io/components/wifi.html#connecting-to-multiple-networks)

### Requirements
- ESP32 module
- ESPHome 2022.12.0 or newer
- MQTT broker

### Recomendations
- HomeAssistant 2022.12.0 or newer
- ESPHome add-on for HomeAssistant


### References
- https://github.com/fsaris/home-assistant-awox
- https://github.com/Leiaz/python-awox-mesh-light
- https://github.com/vpaeder/telinkpp
