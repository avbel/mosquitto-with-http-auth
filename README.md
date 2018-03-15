# mosquitto-with-http-auth

Docker image of MQTT broker [mosquitto](https://mosquitto.org/) with compiled [mosquitto-auth-plug](https://github.com/jpmens/mosquitto-auth-plug) (only `http` backend).

Use it as official [eclipse-mosquitto](https://hub.docker.com/r/library/eclipse-mosquitto/) image.

Demo of mosquitto.conf

```
allow_anonymous false

auth_plugin auth-plug.so
auth_opt_backends http
auth_opt_http_hostname web
auth_opt_http_port 8080
auth_opt_http_getuser_uri /mqtt/user
auth_opt_http_superuser_uri /mqtt/superuser
auth_opt_http_aclcheck_uri /mqtt/acl
auth_opt_http_with_tls false
```
