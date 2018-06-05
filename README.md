# docker-hue2mqtt

[hue2mqtt.js](https://github.com/klutchell/hue2mqtt.js) docker images

## Build

```bash
# build for rpi3
make build-rpi3
```

## Deploy

```bash
# deploy on rpi3
docker run --name hue2mqtt \
-v hue2mqtt-data:/root/.hue2mqtt \
-e TZ=America/Toronto \
klutchell/hue2mqtt:rpi3-latest
```

## Parameters

* `-v hue2mqtt-data:/root/.hue2mqtt` - persistent data volume
* `-e TZ=America/Toronto` - local timezone

## Usage

_tbd_

## Author

Kyle Harding <kylemharding@gmail.com>

## License

_tbd_

## Acknowledgments

* https://github.com/hobbyquaker/hue2mqtt.js

