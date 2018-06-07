# docker-hue2mqtt

[hue2mqtt.js](https://github.com/klutchell/hue2mqtt.js) docker images

## Build

```bash
make build ARCH=armhf
```

## Deploy

```bash
docker run --name hue2mqtt \
-v hue2mqtt-data:/root/.hue2mqtt \
-e TZ=America/Toronto \
-e BRIDGE_IP=192.168.86.131 \
-e MQTT_PREFIX=hue \
-e MQTT_URL=mqtt://192.168.86.13 \
-e POLLING_INTERVAL=1 \
klutchell/hue2mqtt:armhf-latest
```

## Parameters

* `-v hue2mqtt-data:/root/.hue2mqtt` - persistent data volume
* `-e TZ=America/Toronto` - local timezone
* `-e BRIDGE_IP=192.168.86.131` - ip address of local hue bridge
* `-e MQTT_PREFIX=hue` - mqtt prefix (default is hue)
* `-e MQTT_URL=mqtt://192.168.86.13` - url of local mqtt server
* `-e POLLING_INTERVAL=1` - polling interval in seconds

## Usage

_tbd_

## Author

Kyle Harding <kylemharding@gmail.com>

## License

_tbd_

## Acknowledgments

* https://github.com/hobbyquaker/hue2mqtt.js

