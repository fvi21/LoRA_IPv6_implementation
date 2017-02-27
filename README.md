# LoRa_IPv6_implementation

## Introduction

LoRa is a Low-power, wide-area network that allows to build systems to obtain data on long distances using low bandwith, providing a long battery life to the nodes. This tecnology has the ability to send short packets using Direct Sequence Spread Spectrum (DSSS) in large time intervals. 

This project aims to implement IPv6 for LoRa networks including  Neighbor Discovery service and basic IPv6 configuration. 

## Objetive

By using RoHC, this implementation will build a table inside the LoRa gateway to map the source IPv6 header to an internal ID which will be used to identify the flow to the end-device.  If the source device changes any section of the header, the GateWay will send that difference to the end device using the same flow ID.

## Components

In order to achieve our goal, we plan to use:

	- 1 Modtronix inAir9 LoRa Modules
	- 1 IC880A module
	- 1 Raspberry Pi 2
	- 1 Arduino uno

## Software Components 

For the initial version of the project, the following software components are planned to be used:

	end-device project - Arduino-LMIC library by matthijskooijman
	https://github.com/matthijskooijman/arduino-lmic

	LoraGateway project - LoRa Gateway project by semtech
	https://github.com/Lora-net/lora_gateway

##Updates
27/02/2017 : 6LoWPAN_IPHC and SCHC implementation for ICMP6 communication between LoRa Gateway and LoRa Node.

09/11/2016 : RoHC base and AES decryption added in LoRa GateWay. The hop limit is not configured.
