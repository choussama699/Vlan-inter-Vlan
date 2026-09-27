# Vlan-inter-Vlan

# Lab 01 - VLAN & Inter-VLAN Routing

## Overview

This lab demonstrates the configuration of multiple VLANs and communication between different VLANs using Inter-VLAN Routing with a Cisco router.

## Topology

* 1 Cisco Router
* 1 Cisco Switch
* 6 PCs
* 3 VLANs
* 2 PCs per VLAN

```text
                 Router
                   |
                 Trunk
                   |
                 Switch
          _________|_________
         /         |         \
     VLAN 10     VLAN 20     VLAN 30
     PC1 PC2     PC3 PC4     PC5 PC6
```

## VLAN Configuration

| VLAN    | Network         | Default Gateway | Devices  |
| ------- | --------------- | --------------- | -------- |
| VLAN 10 | 192.168.10.0/24 | 192.168.10.1    | PC1, PC2 |
| VLAN 20 | 192.168.20.0/24 | 192.168.20.1    | PC3, PC4 |
| VLAN 30 | 192.168.30.0/24 | 192.168.30.1    | PC5, PC6 |

## IP Addressing

### VLAN 10

* PC1: `192.168.10.10/24`
* PC2: `192.168.10.20/24`
* Gateway: `192.168.10.1`

### VLAN 20

* PC3: `192.168.20.10/24`
* PC4: `192.168.20.20/24`
* Gateway: `192.168.20.1`

### VLAN 30

* PC5: `192.168.30.10/24`
* PC6: `192.168.30.20/24`
* Gateway: `192.168.30.1`

## Technologies Practiced

* VLAN configuration
* Access ports
* Trunking
* Router-on-a-Stick
* Inter-VLAN Routing
* IPv4 addressing
* Default gateways
* Connectivity testing

## Configuration Objective

The objective is to separate the PCs into three different broadcast domains using VLANs while allowing communication between the VLANs through the router.

## Verification

Connectivity was tested using `ping` between devices in the same VLAN and between devices in different VLANs.

Examples:

```text
PC1 → PC2
PC1 → PC3
PC1 → PC5
PC3 → PC6
```

Successful communication between different VLANs confirms that Inter-VLAN Routing is working correctly.

## Packet Tracer File

The complete Cisco Packet Tracer topology is available in: vlan and intervlan.pkt

`VLAN-InterVLAN.pkt`
