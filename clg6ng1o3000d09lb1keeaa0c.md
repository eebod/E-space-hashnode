---
title: "How Network Masts work"
datePublished: Fri Apr 07 2023 14:35:40 GMT+0000 (Coordinated Universal Time)
cuid: clg6ng1o3000d09lb1keeaa0c
slug: how-network-masts-work
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1680880197082/6f9a0ca3-b2bf-4ac1-a533-d8b4f1c6e37b.png
tags: network, computer-science, radio, networking, computernetwork, computer-networking, wireless-internet-service-providers-in-nigeria, network-mast

---

> **Any sufficiently advanced technology is indistinguishable from magic.**  
> \- Arthur C. Clarke

I have always been very fascinated with how the internet feels so abstract and is yet so real. How do network providers like MTN, Airtel, GLO, etcetera (in Nigeria), give me access to the Internet over thin air? How do my calls and SMS texts reach the intended person? And more importantly why couldn't all of these be free? These were questions I asked growing up.

I eventually decided to find out these answers myself, and in doing so, I realized things were bigger and not as simple as they seemed on the surface.

At the end of this article, you should have an idea why internet access can't be free, at least at the moment, and the roles those tall giant masts we often see around play in giving us access to mobile internet, sending+receiving SMSes and making cellular voice calls.

Sit tight and stare closely as I unravel this **MAGIC.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680879370068/ab179b3c-0d63-4e7f-a7eb-c9e34db8acb2.gif align="center")

## A TRIP INTO CONNECTION

The very first question that popped into my mind back then, was how exactly were calls able to correctly go from one phone to another? These were the days I had fun playing Bounce and Snake Xenxia on these old phones. Unfortunately, Google wasn't easily accessible back then and even when I did get some access to the search engine, I had more sinister(😈) things to do and almost usually had forgotten. Fast forward to some years back and I intentionally began to find answers to these questions. This article shares those answers.

### Let's dissect a network mast

A network mast is a tall structure, sometimes standing alone, and in some cases it might be part of a tall tree, a tall building or just anything strong enough to carry communication components like a radio unit, antenna, or any other equipment used in telecommunications.

It also it has to be tall enough to have very minimal obstruction from buildings, all these so it can easily transmit and receive wireless signals from and to devices over long range.

While searching, one of the articles I came across was a detailed page from [Vodafone](https://www.vodafone.co.uk/network/network-improvements) on network mast components and what each did. Rather than re-invent any wheel, I would give a simpler summary of what those components are and what they did here. A reference to the article would also be referenced below.

### What makes up a network mast

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680810953962/40ef78dc-aa74-4c28-9d9d-067059c6035e.jpeg align="center")

1. #### Antenna
    
    The antennas send calls, texts and internet data to your smartphone or just any device that can talk to a mast, like Mifi's, Routers, laptops and sim enabled IoT devices, using radio waves. The antenna can in turn receive radio waves from containing data payload as well. The higher up an antenna is, the further signal can go. Most masts will have at least three antennas to provide coverage in different directions.
    
2. #### Radio unit
    
    The radio unit generates the radio waves transmitted by the antennas. It is responsible for converting signals between the wireless devices and the network, amplifying the signal, and transmitting it to the base station. Similarly, it receives signals from the **base station** and converts them into a form that can be transmitted wirelessly to devices.
    
    A **base station** is an equipment typically located within or near a network mast, serving as a central hub that manages communication between wireless devices and the mast network. Additionally, it provides authentication and security for wireless connections.
    
3. #### Transmission/backhaul
    
    Cables, traditionally copper but now far more likely to be fiber optic, are used to connect one mast with other masts within the network. They are usually buried in the ground, and a few of us have likely seen cables being laid close to public roads, mostly in multiple colored pipes. In a few cases where it is not feasible to use cables laid in the ground, a microwave dish is used instead, more on that below.
    
4. #### Cabin/cabinets
    
    At the ground level, these contain computers that co-ordinate communication with other masts in the network. Additional equipments, such as a battery backup in case of a power failure and connectors for the transmission/backhaul, are also stored here.
    
5. #### Power
    
    Most masts will draw their power from the National Grid (unfortunately, in Nigeria, our power grid collapses every market Friday); In this case, there is provision for a more reliable power source on-site, mostly diesel generators.
    
6. #### Microwave dish
    
    In some locations, such as remote rural areas, a microwave satellite dish is used instead of fiber optic cables to act as a transmission to connect the mast to the rest of the masts on the network. These dishes transmit data wirelessly over the air using microwaves. To do so, the dish must be within line of sight of a dish on another mast, this means, there can not be any obstructions like houses, trees, poles or anything between the communicating masts. This is the primary reason they are always very tall.
    

The article from Vodafone can be found [here](https://www.vodafone.co.uk/newscentre/smart-living/everything-you-need-to-know-about/mobile-phone-masts-everything-you-need-to-know/).

---

### **How are Phone Calls Connected**?

To answer this, first, you should know that your phone is almost always connected to the nearest network mast with the strongest network signal close to you/it. This also depends on the network provider. It is why you have those small network bar(s) at the top of your phone, it shows how close you are to the mast and how strong the connection signal is. If you are in an area where your phone or device can't reach a network mast from your Telco, you get the **'No Signal'** or **'No Network'** network status.

Also, as earlier stated, every network mast out there is connected to another mast, either via cables or micro waves(wirelessly). You might not see it, but they are all connected and talking to each other over very large distances.

Another crucial part of all this is the Mobile Switching Center(MSC), this is a central control point in the network, it manages call routings, connections between masts, billing, authentication, and overall network management tasks.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680809951556/587cc6e8-e269-452e-aef1-3d83710256ad.jpeg align="center")

Back to the main question, how do calls go from one edge of the country to the other side and get to who we call correctly?

When you call a number, your device(smart-or-not phone) sends a request to the mast it is connected to as we mentioned earlier. That mast forwards that call to the nearest base station which checks that you have the correct permissions and requirements to make the call. When this is confirmed, the base station assigns the caller a frequency channel and then forwards that call to the Mobile Switching Center (MSC). The MSC does its own integrity checks as well and if it passes, it goes ahead to determine the routing path for the call.

A route is all the masts a call needs to pass through to get from your phone to the mast where the number you're calling is connected to. Upon finding this route, it directs the call through it. Once the call request reaches the mast connected to the number called, the mast sends the call notification to the device that has the number being called, prompting it to ring and alert the user of the incoming call.

For a little more technical on how the calls move, let's highlight the main processes:

* **Initiating the Call:** When you start a call, your phone sends a radio signal to the nearest network mast it is connected to. The mast picks up the signal and sends it to the nearest base station via wires or wirelessly with microwaves.
    
* **Authentication:** The base station ensures your phone is allowed on the network, by asking for credentials from your sim card, it then assigns it a frequency channel and a time slot.
    
* **Call Routing:** The base station sends the call to the mobile switching center (MSC), which is responsible for routing the call to its destination.
    
    For example, MTN has numerous Mobile Switching Centers across the country, these control centers receive calls from the base station, find where the person the call is meant to get to is in the country, and how many masts to get to that person, it then sends the call in that direction.
    
* **Mast Routing:** In this case, there are two main scenarios, one is if the individual being called is within the same mast range as the caller, then the call doesn't have to leave that mast, if not, the call hops from one mast to another as the MSC directs.
    
* **Call Termination:** When the call is over, your phone sends a signal to the network indicating that the call has ended. The network releases the frequency channel and time slot assigned to your phone.
    

The quality of a call is dependent on factors like signal strength(the distance between a phone and the closest mast), interference, and the length of the route it takes. If the signal is weak, the voice quality may be poor or the call may get dropped.

All of the above is what happens when you make a call from one phone number to another, it's also almost the same thing that happens when a SMS(Short Message Service) is sent, with some underlying protocol difference, such as sim cards not requiring real time connection and that there is a holding area for sms, where messages are kept if the recipient is offline(maybe their phone is dead, or they are in an area with bad network coverage).

For Internet connection, it's also almost the same, but with some interesting extra touch of complexities and changes, let's check that out.

---

### How you access the Internet with just a SIM and Network Masts

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680845784600/7c4883da-060d-4443-b82b-ce548e9d3578.png align="center")

Every time we use **mobile data**, that's internet access to your mobile phone via the SIM(Subscriber Identity Module) provided by Telcos like MTN, Airtel and the likes in Nigeria. Here, some radio magic and really complex engineering happens.

When you or anybody access the internet, it simply means you have access to files on the **INTER**connected **NET**work, a connection of millions of computers around the world. For example, this means you can reach and talk to computers owned by Google, allowing you access to their applications as well. Examples of those are: Google's search engine, Youtube, GMail, Google Cloud, and many more.

On the internet you can access not just Google's computers though, you have access to Wikipedia, Zoom, TikTok, Linkedin, Facebook, Amazon, Jumia, Bolt, Uber and millions of other websites.

You can get access to these applications on their powerful computers(servers) because they are publicly available on the internet. You also have the ability to send files to those computers (**UPLOAD**) or pull down files from them(**DOWNLOAD**), which is mostly what we all do. You download when you watch, reels, shorts, stream movies etcetera, and you upload data when you change your profile picture, post to your Whatsapp status, post reels, youtube, videos and share memes.

The internet is not some magic, but rather a well thought through connections of fibre cables between continents laid on the sea floor. These cables are the backbone of the internet, managed by ISPs, data centers or service providers within each countries on the continents they land.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680858690329/b51dfd8b-080c-4989-bfeb-3d2c0d284bd3.png align="center")

⬆️ | [Image](https://www.submarinecablemap.com/) showing the Fiber cables under the sea, powering the internet.

How your device reach those servers over the available number of cables, via the mast, is in itself a networking topic deserving a write up of its own. It is a beautiful and very well executed feat of network engineering handled by large companies around the world.

For now, we'll just talk discuss the role the network masts deployed by telcos to extend their network, play in the whole process.

* When you access the internet(assuming you still have an active data **subscription**), the data allows you to speak to the mast which passes on that request to other masts.
    
* The data is then processed by the radio unit(I talked about radio units earlier up) on the network mast, which converts the data from digital to analog signals that can be transmitted over airwaves.
    
* The data is then transmitted to other network masts and base stations which serve as a gateway to the ISP's core network.
    
    The core network is typically made up of multiple interconnected data centers and high-performance equipment and infrastructures designed to handle large volumes of data traffic, responsible for managing the routing of data traffic within and between networks.
    
* The data is routed through the ISP's core network to an internet gateway( a component that connects the ISP's network to the internet).
    
* The internet gateway sends the data out onto the internet, where it reaches the destination server for the requested data, most often across the world.
    
* The data travels back through the ISP's core network and is routed to the appropriate base station and network mast to reach the user's device.
    
* Your phone receives the requested data.
    
    This entire process occurs within a matter of seconds.
    

To make this quite relatable and practical, we'd use Whatsapp. Let's try a scenario where we download a voice message(an audio file) from a friend using MTN's network

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680864492972/23e870af-4f7b-4068-803f-07b3d982b1db.png align="center")

➡️ | You open Whatsapp, where you received a voice message from a friend.

➡️ | You tap the download icon, and then WhatsApp sends a data request from the application through your phone, to the network mast your phone is connected to, managed by either MTN, Airtel, GLO or any other Telco. This request is transmitted as radio waves over the air from your phone to the network mast.

➡️ | The network mast receives the request and forwards it to the nearest base station, which serves as a gateway to MTN's core network.

➡️ | The request is then transmitted across the MTN core network to an internet gateway, which connects the MTN network to the internet.

➡️ | The internet gateway sends the request out onto the internet, where it reaches a WhatsApp server, these servers are located in data centers across the world, in places like the United States, Europe, and Asia. So depending on which server the voice message is on, the request would most likely pass through fiber cables under the sea to get it.

➡️ | WhatsApp server finds the voice message you asked for and sends it back through the internet to MTN's network.

➡️ | The voice message travels back through the MTN's core network and is routed to the appropriate base station and network mast to reach your phone.

➡️ | Your phone receives the voice message and stores it in storage so you have it permanently, and then move it to memory allowing you to listen to it.

This happens for everything you download on your phone, image, video, audio, sticker, voice message, even when you make voice and video calls on WhatsApp or on any other application on your device.

The best part about all of this is that it happens so fast, you don't even know what just happened. The under-sea fibre cables move data around at the speed of light.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680862622916/2caeff0c-3047-4ab2-817d-c01461e4df12.jpeg align="center")

Without network masts, the majority of all of us wouldn't be able to efficiently do the everyday things we do. Things like making calls, sending texts or using the internet. This is slowly changing though, as there are already things like FTTH(Fiber-To-The-Home) where you have a wired connection to your house to access the internet instead, there is also now a growing battle of satellite internet projects with the likes of [HughesNet](https://www.hughesnet.com/), [Viasat](https://www.viasat.com/), [Starlink](https://www.starlink.com/), [Oneweb](https://oneweb.net/), [Telesat](https://www.telesat.com/), [Project-Kuiper](https://www.aboutamazon.com/what-we-do/devices-services/project-kuiper) etcetera. Also, we have our popular easy to use Wifi/Hotspot network too that we could quickly use to share files with a friend.

### **Then why do we pay for internet I still hear you ask?**

If you didn't figure that out yet, yeah, let's talk about it. Earlier on we talked about network masts, first, those things are expensive to set up, getting a piece of land to set them on, the structure and the work to get them up, the cost of the antennas, radio unit, the cost of a backhaul if used(having to dig the ground and lay cables to connect one mast to another), cost of cables, costs of generators, the cost of fueling, there is a need to put someone on salary to constantly monitor the premise and maintain the system.

While writing this article, I came across a news write-up where thieves walked into a network mast premise to steal diesel meant to power the backup generators, and that's just the light side of the vandalism, it gets worse.

They also have to pay engineers to manage the hardware and software sides of everything.

It also cost an awful lot for Telcos to purchase spectrum licenses, I mean (1G, 2G, 3G, 4g and currently 5G), the most recent 5G spectrum license MTN had to buy from NCC, cost over 200 Million dollars, Airtel bought as well, and they have had to buy licenses all through the spectrum band to 5G.

When you add all of these things up and multiply it across all the network masts you see around and you can very quickly see a large startup and running cost emerge.

One other thing, companies like MTN, Airtel, GLO, etc might not also connect directly to the internet, they also connect to other ISPs for service, it's a hierarchical order of connection, and there are tiers to it, if they do not connect directly, they have to pay for connections.

Also we mentioned sub sea cables earlier. Running and maintaining these types of cables connecting one continent to another, cost millions of dollars.

A clearer image should have appeared by now, as to how much it costs to start and run a Telecommunication or Internet Service providing company. It is both capital-intensive and also running-cost-intensive, to stay sustainable and run at a profit, we the users have to pay to use the service.

This is why we pay to use the internet, pay for airtime to make calls and send SMS.

**FunFact:** It is called **airtime** because when you make a voice call, use the internet or take a call, your phone uses radio waves to communicate with the cellular network over the **'air'**. How long you can do that, the **'time'** is based on how much you pay. |😌|

If you read it all to this point, thank you..💪🏾..

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680864966845/442d0907-38b9-4537-8071-ba6084828b46.gif align="center")

It feels like a very long one, but it was fun writing this, I hope you picked something.

> And you, yeah you, if you're seeing this, hmmm. It's .......