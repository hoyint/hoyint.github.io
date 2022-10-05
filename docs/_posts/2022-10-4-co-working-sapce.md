---
title: Co-working Space Design
tags: [structured cabling, rack]
style: border
color: warning
description: A overview of a project I design and implemented for a co-working space.
---

# Introduction

The client requires a full set of IT services for their co-working space business. The client has a customer relationship management(CRM) system that allows customers to directly rent or lease spaces. The client requires all IT services to be integrated into their CRM platform.

The problems:
- Design a network to support a high traffic of users and integrate with the clients CRM.
 - Prompt customer credentials network access when customers access network via Ethernet and WiFi.
- Integrate access control systems to CRM so that customers can access the building via their phone base on the CRM permissions. 
- Set up media system for the co-working space

## Designing the network
The client requires the network to be highly available while also being flexible for future expansions. 

### Dedicated IT rooms
Before construction it was discussed with the client that every floor of the co-working space should have its own IT room that would house all of the related IT equipment for its respective floor. Critical equipment such as routers (layer 3) would remain in the server room. Having dedicated IT rooms for each floor would allow for easy future expansion and remove the necessity of running cables across each floor, instead if a device needed to be added then a cable can be ran to the IT room of the respective floor.

<div style="display:flex">
     <div style="flex:1;padding-right:10px;">
          <img src="/images/network-closet.jpeg" width="500"/>
     </div>
     <div style="flex:1;padding-left:10px;">
          <img src="/images/network-closet2.jpeg" width="500"/>
     </div>
</div>
The service loops were specifically ran that way because the client was not sure if the IT racks would be moved, for simplicity of moving the racks the service loop was not coiled. 

### ISP
The location only has DSL and dedicated fiber, the speed of DSL is not sufficient for the clients use case. It was recommended to the client that they would also need two(2) dedicated fiber lines from two(2) different ISPs for network redundancy.

## Access Control System
In the fields of physical security and information security, access control (AC) is the selective restriction of access to a place or other resource, while access management describes the process. The act of accessing may mean consuming, entering, or using. Permission to access a resource is called authorization[^fn1]. 

Kisi was the integration that was used as it was the simpliest and most efficient. The CRM communicates with Kisi via Kisi's API, it allows the CRM to add and remove customer permissions for the customers mobile app.

<div style="display:flex">
     <div style="flex:1;padding-right:10px;">
          <img src="/images/kisi-credentials.jpeg" width="500"/>
     </div>
     <div style="flex:1;padding-left:10px;">
          <img src="/images/kisi-wiring.png" width="500"/>
     </div>
</div>

## Media System
Bose speakers were used for each floor, each floor has its own bose amplifier. The client required a public address(PA) system, to do this a SIP paging gateway was used. The SIP paging gateway is a device that can send a trigger signal to the amplifier to stop or reduce the sound and relay the audio that the SIP device is receiving. SIP is a ip protocol that allows users to commincate via voice or video on a network.

[^fn1]: https://en.wikipedia.org/wiki/Access_control