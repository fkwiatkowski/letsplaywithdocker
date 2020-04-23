FROM alpine:latest

# --no-cache to reduce size
RUN apk --no-cache add mosquitto

# Client connections through host command line
# RUN apk --no-cache add mosquitto-clients

# Export MQTT and MQTTS ports
EXPOSE 1883
EXPOSE 9883

# Update PATH
ENV PATH /usr/sbin:$PATH

# Launch mosquitto broker
ENTRYPOINT ["/usr/sbin/mosquitto"]

