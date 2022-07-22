# Pulse

Web-RTC based Video Conferencing and File Sharing System.

This uses Public (or declared) STUN Servers to initiate connection between Client Browsers. After the initial connection, all data is shared directly between the Client Browsers with no intermediate Server in the middle. Connecting to unreachable networks is handled by using an exponential backoff when sending the subsequent connection requests after the initial connection establishment fails. This is usually a problem faced when trying to connect to machines inside or outside a NAT gateway. TURN Servers are not supported at the moment.

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
