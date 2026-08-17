# SOC Lab Architecture

## Overview

This project is a virtualized Security Operations Center (SOC) lab built with VirtualBox and Wazuh

The lab contains a Wazuh Manager and two monitored endpoints:

- Wazuh Manager — Debian
- Client1-W — Windows
- Client2-L — Linux

## Network Architecture

The virtual machines communicate through a dedicated VirtualBox NAT Network

| Machine | Operating System | IP Address | Role |

| WAZUH-SERVER | Debian | 192.168.1.19 | Wazuh Manager |
| Client1-W | Windows | 192.168.1.20 | Monitored endpoint |
| Client2-L | Linux | 192.168.1.21 | Monitored endpoint |

Network:

`192.168.1.0/24`

Gateway:

`192.168.1.1`

## Wazuh Communication

The Wazuh Manager exposes the following services:

- TCP/UDP 1514 — Wazuh agent communication
- TCP 1515 — Agent enrollment
- TCP 55000 — Wazuh API

## Connectivity Validation

Connectivity between the Wazuh Manager and Linux endpoint was successfully validated

The Wazuh Manager is reachable at:

`192.168.1.19`

The Linux endpoint is reachable at:

`192.168.1.21`

TCP connectivity to Wazuh ports was also validated from the Linux and Windows endpoints

## VirtualBox Network Design

The lab uses two network interfaces on the virtual machines:

- NAT — Internet access
- NAT Network (`NatNetwork`) — communication between SOC lab machines

This separation allows the endpoints to communicate with the Wazuh Manager while maintaining Internet connectivity for updates and installation.