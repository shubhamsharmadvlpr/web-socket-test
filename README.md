# web-socket-test
Docker-image for WebSocket connectivity test.

## How to
### Start contaienr
```bash
$ docker run -p 8010:8010 --name web-socket-test reaper7/web-socket-test:v1
```

### Connect to container with WebSocket
```bash
$ npm install wscat
$ wscat --connect ws://$(CONTAINER_HOST_IP_ADDRESS):8010

connected (press CTRL+C to quit)
> Hello world

< Server received from client: Hello world
>
```

### Check your container log
```javascript
npm info ok
Server started
Received from client: Hello world
```
It works!!!
