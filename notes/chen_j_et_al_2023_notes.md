Networked Architectures for Localization-Based Multi-User Augmented Reality
(Chen J. et al, 2023) https://ieeexplore.ieee.org/document/10375692

---

Abstract:
- This article is about mapping out different system architectures on how to build AR-apps with multiple users, where user location is important.

Introduction:
- Multi-user AR: multiple users join the same AR session, interacting with the same set of AR holograms.
- In order to draw the AR-holograms to the right places, AR devices need to know their location in the real world and map them to the AR world. In multi-user AR all the devices sharing the AR session must also communicate their locations with each other. All this must also happen quickly and accurately.
- Edge Cloud (EC; the act of moving servers/processes physically closer to the end user, lowering the latency) is presented as a potential enabler of latency-sensitive, multi-user AR
- Goals of this article:
  - Provide theoretical background on AR localization os single-user and multi-user AR, illustrate involved latency & accuracy issues
  - Describe system architectures for multi-user AR location calculations
  - Describe AR use-cases, their latency & accuracy requirements & the ability of the proposed architectures to meet the needs of these use cases

Background on AR Localization:
AR Platform Architecture:
 - Layers of multi-user AR platforms: Inputs (camera, mic, etc), are utilized by: AR platforms (unity, unreal etc.), which are used to build apps, instances of which communicate with each other using the cloud
 - In certain instances of multi-user AR (vechicle driving)fast & accurate communication is a requirement
Single-User Localization:
 - Consists of two steps:
   - Tracking
     - A client determines its pose in the real world by datamininig image features from the client's camera feed.
   - Mapping
     - Create a 3D representation of the real world based on the info from tracking whenever new information is encountered in tracking.
Multi-User Localization:
 - Multiple users perform Single-User Localization first, then synchronize their internal maps (output of Single-User Localization's "Mapping" task) to create a "global map" coherently shared between all users.
 - Algorithm for merging local maps of two Multi-User AR Clients:
   1. Client A gathers real-world data
   2. Client A places hologram
   3. Client A sends real-world data (visual information) and hologram data (pose, geometry, textures) to EC-server
   4. EC-server processes Client A's data into global map using SLAM
   5. Client B gathers real-world data
   6. Client B sends real-world data to EC-server
   7. EC-server adds new data from Client B into global map (A's map)
   8. EC-server sends client B the global map
   9. Client B can now see the hologram placed by client A in the correct position & orientation
 - The process works the same way with more then two users: Local tracking and mapping are performed and the EC-server gets updated  whenever there is a change. the EC-server then broadcasts the global map to all the clients.
 - Updating the global map (both on a client and on a server level) can be computationally expensive, and requires a fast network!

Networked Architectures for Multi-User AR:
 - This paper proposes three different network architectures for multi-user AR. The differences between these architectures is the location where the global map gets constructed and what information needs to be communicated between different clients.
Edge-Cloud Centric:
 - In this approach, both tracking and mapping is performed by the EC-server. The only job of the clients is to gather data and draw the map received from the server.
 - Whenever there are network delays slowing down the receiving of global map data from the server, the clients use their Inertial Measurement Units (IMUs) to approximate the state of the global mep
 - The EC-server stores the global map on a shared memory buffer. that way all slients can simultaneously access it leading to more efficient synchronization across the system
Edge-Cloud Assisted:
 - This model performs the tracking and some mapping on the client devices. However the global map gets generated on the EC-server. Global map generation uses local map data sent from the clients. The EC-server sends the global map back to the clients. Thus this method too requires a lot of datatraffic.
P2P:
 - In this model there is no EC-server. Instead all clients receive data from all other clients. Either there is no centeral authority and all clients must construct the global map for themselves or one of the clients acts as an EC-server for some duration (typically one session)

Use cases: 

---

Lyhenteet:
EC		Edge Cloud
IMU		Inertial Measurement Unit
SLAM	Simultaneous Localization And Mapping
