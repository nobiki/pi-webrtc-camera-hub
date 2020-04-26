# pi-webrtc-camera-hub

#### Install Node Package

```
$ direnv allow

$ npm i socket.io
```

#### Dnsmasq Settings

```
$ vim docker-compose.yml

// Change IP address
services:
  camera-hub-dnsmasq:
    extra_hosts:
      - "camera-hub.local:192.168.2.204"
      - "socket.camera-hub.local:192.168.2.204"
```

#### Start WebRTC

```
$ docker-compose up -d
```

Check if you can access the domain you set

* [https://camera-hub.local](https://camera-hub.local)
* [https://socket.camera-hub.local/socket.io/socket.io.js](https://socket.camera-hub.local/socket.io/socket.io.js)

