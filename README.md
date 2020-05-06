# pi-webrtc-camera-hub

[古いスマホをWebRTCで監視カメラにした時のメモ | 7me](https://7me.oji.0j0.jp/2020/05/06/webrtc-smartphone-camera-memo/)

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

