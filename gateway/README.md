##Packet_forwarder
Dockerfile for packet_forwarder which will run packet_forwarder with default env settings specified in file.
###Build image
'sudo docker build -t packet_forwarder:alpha -f Dockerfile-packetforwarder .'
###Test Run container
'sudo docker run --privileged --name forwarder --device /dev/spidev0.0:/dev/spidev0.0 --device /dev/spidev0.1:/dev/spidev0.1 --rm -it packet_forwarder:alpha'
###Daemon run container
'sudo docker run --privileged --name forwarder --device /dev/spidev0.0:/dev/spidev0.0 --device /dev/spidev0.1:/dev/spidev0.1 --restart=on-failure -d packet_forwarder:alpha'

##TODO
[] Create file for broocar gateway
[] Solve issue with central logging
[] Intercept gRPC messages