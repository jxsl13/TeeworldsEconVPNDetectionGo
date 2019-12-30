## Requirements
 - Redis server for caching of IPs
 - .env file in te same folder as the executable

## Example .env
This file needs to live within the same directory as yout executable.
```
# .env
IPHUB_TOKEN=abcdefghijklmnopqrst0123456789
EMAIL=john.doe@example.com

SERVER_LIST=127.0.0.1:9303 127.0.0.1:9304 127.0.0.1:9305
PASSWORDS=abcdef0123456789
RECONNECT_TIMEOUT_MINS=1440

REDIS_ADDRESS=localhost:6379
REDIS_PASSWORD=


VPN_BAN_TIME=1440
VPN_BAN_REASON=VPN - discord.gg/ThGZ45e
```
Either use one password for all servers or one password per server.

## Downloading dependencies
```
go get -d
```

## Building
```
go build .
```

## Running
```
./TeeworldsEconVPNDetectionGo
```

## Troubleshooting

##### EOF error
The Teeworlds server banned you for attempting to login too any times or for connecting too often.
Possible solution is to restart the game server. Should not be an issue, as the detector attempts to reconnect to the server.
