# Projeto Prático RCD 2025/2026

![UMa](https://img.shields.io/badge/Universidade_da_Madeira-RCD_2025%2F2026-blue)

---

## Table of Contents

- [About the Project](#about-the-project)
- [Network Topology](#network-topology)
- [IP Addressing](#ip-addressing)
- [Roadmap](#roadmap)
- [Contributors](#contributors)

---

## About the Project

This project simulates a distributed network across two geographic locations — **Aveiro** and **Covilhã** — connected via the Internet through ISP routers (VOD and MEO).

The first phase focuses on IP address planning using **VLSM (Variable Length Subnet Masking)**, a technique that allows subnets of varying sizes to be created, minimising address waste.

### Highlights

- VLSM subnetting for two locations
- 6 subnets per location (VLANs)
- Physical topology built in Cisco Packet Tracer
- Router-on-a-stick configuration (AVR and CVL)
- ISP connectivity via Serial links (VOD and MEO)

---

## Network Topology

![Network Topology](https://media.discordapp.net/attachments/1479506594097004624/1494050070008434709/image.png?ex=69e1320e&is=69dfe08e&hm=41df5740c1c14d596de168da8771fe3dfb37703e4245f5e1c3df5f933e827016&=&format=webp&quality=lossless)

---

## IP Addressing

### Aveiro — `10.99.9.0/24`

| Subnet | VLAN | Hosts | Network | Mask | Gateway |
|--------|------|-------|---------|------|---------|
| Quiosque | 70 | 38 | 10.99.9.0 | /26 | 10.99.9.1 |
| Guest | 30 | 28 | 10.99.9.64 | /27 | 10.99.9.65 |
| IoT | 503 | 24 | 10.99.9.96 | /27 | 10.99.9.97 |
| Servers | 160 | 15 | 10.99.9.128 | /27 | 10.99.9.129 |
| Printers | 16 | 7 | 10.99.9.160 | /28 | 10.99.9.161 |
| Management | 500 | 7 | 10.99.9.176 | /28 | 10.99.9.177 |

### Covilhã — `10.30.9.0/24`

| Subnet | VLAN | Hosts | Network | Mask | Gateway |
|--------|------|-------|---------|------|---------|
| Guest | 30 | 33 | 10.30.9.0 | /26 | 10.30.9.1 |
| Management | 500 | 33 | 10.30.9.64 | /26 | 10.30.9.65 |
| Servers | 160 | 31 | 10.30.9.128 | /26 | 10.30.9.129 |
| SOC | 100 | 15 | 10.30.9.192 | /27 | 10.30.9.193 |
| Security | 502 | 12 | 10.30.9.224 | /28 | 10.30.9.225 |
| Printers | 16 | 9 | 10.30.9.240 | /28 | 10.30.9.241 |

---

## Roadmap

### Phase 1 — IP Planning
- [x] VLSM subnetting for Aveiro and Covilhã
- [x] IP addressing tables for all devices
- [x] Physical topology in Cisco Packet Tracer

### Phase 2 — Network Configuration
- [ ] Basic device configuration (hostname, SSH, NTP, passwords)
- [ ] Router interfaces and sub-interfaces (802.1Q)
- [ ] DHCP server configuration
- [ ] DNS and HTTP server setup
- [ ] VLANs and trunk configuration
- [ ] Link Aggregation (LACP)
- [ ] RIP V2 routing
- [ ] NAT Overload (PAT)
- [ ] Connectivity tests

---

## Contributors

| Name | Student No. |
|------|-------------|
| **Mário Belim** | 2173324 |
| **Lucas Silva** | 2146224 |
| **Francisco Gouveia** | 2178724 |

**Group 9 — PL2 | Universidade da Madeira**
Professors: Lina Leão & Lisandro Marote

---

*Redes e Comunicação de Dados 2025/2026*
