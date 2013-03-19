Readme
Ensure that the number of threads is enough
- esigate.properties
- app server connector
Ex: if you are launching ab with "-c 30" you should set maxConnectionsPerHost=30 and connector max threads =60

You can launch jetty 9 with "mvn jetty:start"
 
Test command lines:
ab -c 30 -n 1000000 http://localhost:8080/esigate-performance-tests/esigate/test.html
ab -c 30 -n 1000000 http://localhost:8080/esigate-performance-tests/esigate-nocache/test.html

Note: run each command twice waiting a few seconds. This will warm up the server.