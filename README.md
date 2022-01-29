# snapcast-docker


## Compose

```
version: "3"

services:
  snapclient:
    image: hbdk/snapcast-client:latest
    hostname: <Your desired name this client>
    restart: unless-stopped
    devices:
      - "/dev/snd:/dev/snd"
    command: -h 192.168.1.113 --sampleformat 48000:16:*
```