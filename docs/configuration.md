---
layout: default
title: IP Addressing Methodology
nav_order: 2
---

# IP Addressing Methodology 
### [Return Home](index.md)

This web page is my attempt to help everyone understand my thought processes behind how I evaluate requests to determine the IP Addressing space I will allocate. (Feel free to read the [FAQ](#faq) at the bottom to help explain some terms used)


1. To preserve the Missouri `44.46.0.0 /20` address space, I generally will only allocate space to operators will are intending on routing beyond their local (home) network.
2. Allocations will be assigned in CIDR blocks within the range of `/32`-`/24`. Where feasible, a buffer of unused ad- dresses will be maintained above assigned blocks to allow for future growth. (See [FAQ](#faq) below for CIDR info).  Current assignments are being made as follows:
  * `/32` & `/30` - `44.46.0.x`
  * `/29` - `44.46.1.x`
  * `/28` - `44.46.2.x`
  * `/24` - `44.46.16-100.x`
3. Subnets will be based on connectivity to a server (gateway, switch, or other full-time service provider).
4. To ensure that all hostnames are unique, they must include an amateur radio callsign. Compound hostnames (e.g., "switch.k8you.ampr.org") are acceptable. (Exceptions will be made where there is no possibility of duplicate hostnames.)
  * Hosts may be given aliases like "switch.stlouis.ampr.org" through locally maintained CNAME records. These CNAMEs will be for local use only and will not be propagated to the master domain name server.
5. Assignment of hostnames within subnets will ordinarily be delegated to a person local to that subnet.
  * That person should report address assignments to the state coordinator.
  * All addresses that are issued in accordance with these guidelines, and reported to the state coordinator, will be submitted to the ampr.org database. No one other than the state coordinator can update the database.

# FAQ
* What is a CIDR notation?
  * [Classless Inter-Domain Routing (CIDR /ˈsaɪdər, ˈsɪ-/) is a method for allocating IP addresses and for IP routing.](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing)
* CIDR Blocks
  * `/32` Allocates `1` IP Address
  * `/31` Allocates `2` IP Addresses
  * `/30` Allocates `4` IP Addresses
  * `/29` Allocates `8` IP Addresses
  * `/28` Allocates `16` IP Addresses
  * `/27` Allocates `32` IP Addresses
  * `/26` Allocates `64` IP Addresses
  * `/25` Allocates `128` IP Addresses
  * `/24` Allocates `256` IP Addresses

## Future Considerations
* Other states coordinate Subnet space in groups based on region of use.  Was contemplating using the [Missouri Highway Patrol Troop map](https://www.mshp.dps.missouri.gov/MSHPWeb/DevelopersPages/TroopHeadquarters/troopIndex.html) as a guide.
  * Northern Missouri: Troop H & B
  * Central Missouri: Troop A, F, C
  * Southwest Missouri: Troop D & G
  * Southeast Missouri: Troop E & I
