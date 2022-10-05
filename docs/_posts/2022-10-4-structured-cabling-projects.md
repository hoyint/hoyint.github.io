---
title: Overview of some of my structured cabling projects.
tags: [structured cabling, rack]
style: border
color: light
description: A overview on some of my structured cabling projects.
---

# Introduction

In telecommunications, structured cabling is building or campus cabling infrastructure that consists of a number of standardized smaller elements (hence structured) called subsystems. Structured cabling components include twisted pair and optical cabling, patch panels and patch cables[^1].

## Multi-site Camera System Overview
The client required a reliable camera system for multiple sites from various geographical locations. Each site had at least four(4) floors and every floor required minimum 20 cameras, which averaged to 80 cameras per site. I was tasked with desinging and implementing a system  that would not cause any desruptions to the day to day operations and allow the system to be centrally managed. 

### Problems and Solutions
The problems:
- How to network all the cameras
- Centrally manage all the cameras 

#### How to network all the cameras
We needed a way to efficiently implement a camera network without causing any desruptions. To efficiently do this we designated a room on each floor that would house the patch panel and switch for the cameras on that floor. From each floors designated room we would have a trunk cable to the server room to connect all the cameras to the central system. 

##### Why create a DMARC on each floor
Creating a DMARC on each floor makes running cables for each camera easier, instead of having to run 100 cables across 5 floors to reach the server room we only needed to run 5 cables from each DMARC room to the server room. The added benefits of this is that we were able to save space in the server room conduit, more quickly get the infastructure operationaly and save on cabling. 

{% include elements/figure.html image="/images/camera-network.jpeg" caption="Camera Network with DMARC" %}

##### DMARC Racks 
A few images of the racks and cabling I have installed. 

<div style="display:flex">
     <div style="flex:1;padding-right:10px;">
          <img src="/images/demarc1.jpeg" width="500"/>
     </div>
     <div style="flex:1;padding-left:10px;">
          <img src="/images/demarc2.jpeg" width="500"/>
     </div>
</div>

#### Centrally manage all the cameras
Every site has their own video storage device for their respective sites cameras, however the client requires access to all cameras on a centralize platform without exposing the system to the internet. To do this we install a management server on one of the sites and use the existing MPLS connect across all sites to connect the video storage device to the management server. THe management server allows the client to create users and user policies to ensure that staff with the proper permissions are able to view the cameras. 

{% include elements/figure.html image="/images/camera-overview.jpeg" caption="Camera Network with DMARC" %}



# Footnote


[^1]: https://en.wikipedia.org/wiki/Structured_cabling