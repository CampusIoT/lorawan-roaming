# Simple-as-possible LoRaWAN roaming with Chirpstack

## Context
LoRaWAN roaming enables to forward endpoints' frames from one LoRaWAN network to another. LoRaWAN roaming is specified by the LoRa Alliance into  two specifications ([Back-End Interfaces standard](https://lora-alliance.org/resource_hub/ts002-110-lorawan-backend-interfaces/) and Roaming Hub Technical Recommendation Draft).

## Description
This program provides a simple way to forward `DataUp` frames (ie not `JoinRequest`/`JoinAccept`/`DataDown` frames) for a Chirpstack (visitor) network server to another network. The visitor network server should be registered as LoRa gateway (one or many) into the home LoRaWAN network. The visitor network server acts as a macro-gateways.

This program is based on:
* Docker and Docker Compose
* NodeRED
* InfluxDB (optional for monitoring and accounting)
* Grafana (optional for monitoring and accounting)

## Usage

1) Install Docker and Docker Compose

2) Change the default credentials into NodeRED and Grafana

3) Launch the composition
```bash
docker-compose up -d
docker-compose ps
docker-compose logs -f
```

4) Configure into the NodeRED flow
* the MQTTs credentials,
* the list of visitor gateways,
* the DevAddr whitelist (NetID, DevAdddr range or DevAddr list)

## NodeRED and Grafana Credentials
### NodeRED
TODO

### Grafana
TODO
