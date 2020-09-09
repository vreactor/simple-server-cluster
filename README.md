
# Simple server with clustering on Node.js

Using the cluster module to create a failover server on Node.js that can withstand heavy loads.

## Load shooting on the server

[autocannon](https://www.npmjs.com/package/autocannon) - benchmarking tool

autocannon -c 200 -d 10 [http:\\localhost:8800](http:\\localhost:8800)

## Testing

- node cluster.js
- autocannon -c 200 -d 10 http:\\localhost:8800
- kill `<PID>` // Kill the process
- kill -s SIGUSR2 `<PID>` // Kill the process and restart the worker
