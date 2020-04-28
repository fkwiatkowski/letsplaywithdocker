# letsplaywithdocker  
Various examples and tests about Docker

## mqttalpine  

Simple dockerfile to run a mosquitto broker  

### Build

```bash
docker build --no-cache --tag "mqttalpine:latest" .
```

### Run  

```bash
docker run -p 1883:1883 mqttalpine:latest
```

### Use  

```bash
mosquitto_sub -h <hostip> -t "testdocker"
mosquitto_pub -h <hostip> -t "testdocker" -m "hellobaleen"
```


## makefilealpine    

Simple dockerfile that clone a git repo, compile source code and run executable using multistage dockerfile

### Build

```bash
docker build --no-cache --tag "makefilealpine:latest" .
```

### Run  

```bash
docker run makefilealpine:latest
```

### Standard output   

```bash
$ docker run "alpinemake:latest"
[Template Makefile] : main.c : Hello World

[Template Makefile] : tools/tools.c : dummyprintf
```
