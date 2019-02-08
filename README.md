# This is an example and is not ment for production use in this state

This is a sample configuration for running nginx to proxy through to some service.

It contains certificates, however if you need to generate new ones use the following commands

```
openssl genrsa -des3 -passout pass:x -out server.pass.key 2048
openssl rsa -passin pass:x -in server.pass.key -out server.key
openssl req -new -key server.key -out server.csr
openssl x509 -req -days 364 -in server.csr -signkey server.key -out server.crt
 ```

