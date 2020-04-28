# letsplaywithdocker  
Various examples and tests about Docker

## mqttalpine  

Simple dockerfile to run a mosquitto broker  

### Build

```bash
docker build --no-cache --tag "alpinemqtt:latest" .
```

### Run  

```bash
docker run -p 1883:1883 alpinemqtt:latest
```

### Use  

```bash
mosquitto_sub -h <hostip> -t "testdocker"
mosquitto_pub -h <hostip> -t "testdocker" -m "hellobaleen"
