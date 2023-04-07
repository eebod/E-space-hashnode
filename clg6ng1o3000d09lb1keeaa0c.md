---
title: "How Network Masts work"
datePublished: Fri Apr 07 2023 14:35:40 GMT+0000 (Coordinated Universal Time)
cuid: clg6ng1o3000d09lb1keeaa0c
slug: how-network-masts-work
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1680880197082/6f9a0ca3-b2bf-4ac1-a533-d8b4f1c6e37b.png
tags: network, radio, networking, wireless-internet-service-providers-in-nigeria, network-mast

---

> **Any sufficiently advanced technology is indistinguishable from magic.**

I have always been very fascinated with how the internet feels so abstract and is yet so real. How do Internet Service Providers like MTN, Airtel, GLO, etcetera (in Nigeria), give me access to the Internet over thin air, and I have to give them my physical cash? Why do they even charge for it? How do my calls and SMS texts reach the person for them? These are questions I asked as I was growing up, but no one around me could answer.

Eventually, I decided to find out these answers myself, and in doing so, I realized things were deeper and sorta more mysterious than they seemed on the surface.

At the end of this article, you should have an idea as to why internet access can't be free, at the moment at least, and the roles those tall giant masts you often see around, play in giving you access to mobile internet, sending and receiving SMS and making cellular voice calls.

Sit tight and stare closely as I show you this **MAGIC.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680879370068/ab179b3c-0d63-4e7f-a7eb-c9e34db8acb2.gif align="center")

## A TRIP INTO CONNECTION

The very first question that popped into my mind back then, was how the heck were calls able to go from one phone to another? They were the days I had fun playing Bounce and Snake Xenxia on these old phones. Unfortunately, google wasn't easily accessible then and even when I did get access to the search engine, I had more sinister(😈) things to do. Fast forward to some years back and I intentionally began to source answers, I'll share what I did find, and don't worry, you don't have to pay, 'Oluwa lo lope' .🤝🏾.

### Let's dissect a network mast

A network mast is a tall structure, sometimes it might stand alone, something similar to the image that comes below or in some cases, a tall tree, a part of a tall building or just anything high enough that can carry communication components like a radio unit, antenna, and other equipment used in telecommunications to both transmit and receive wireless signals. It is simply those structures, put in place by Internet service providers, that can talk to our phones and other wireless devices and provide network connection.

In my search for information on network masts, I saw a detailed page from [Vodafone](https://www.vodafone.co.uk/) on network mast components. I will simply expand and summarise that here. I would also leave a reference to the main content at the end.

### What makes up a network mast

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680810953962/40ef78dc-aa74-4c28-9d9d-067059c6035e.jpeg align="center")

1. #### Antenna
    
    The antennas send calls, texts and internet data to your smartphone using radio waves and in turn receive radio waves from it. The higher up an antenna is, the more likely it is that you’ll get a strong and reliable mobile signal from it. Most masts will have at least three antennas to provide coverage in every direction.
    
2. #### Radio unit
    
    The radio unit generates the radio waves transmitted by the antennas. It is responsible for converting signals between the wireless device(your phones. etc) and the network, amplifying the signal, and transmitting it to the base station. Similarly, it receives signals from the base station and converts them into a form that can be transmitted wirelessly to the wireless device.
    
    A base station is equipment that is always within a network mast or sometimes between network masts, It acts as a hub that manages communication between wireless devices and the network and also provides authentication and security for the wireless connection.
    
3. #### Transmission/backhaul
    
    Cables, traditionally copper but now far more likely to be fiber optic, are used to connect one mast with other masts within the network. They are usually buried in the ground. In a few cases, a microwave dish is used instead.
    
4. #### Cabin/cabinets
    
    At the ground level, these contain computers that communicate with other masts in the network. Additional equipment, such as a battery backup in case of a power failure and connectors for the transmission/backhaul, are also stored here.
    
5. #### Power
    
    Most masts will draw their power from the National Grid (unfortunately, in Nigeria, our power grid collapses every market Friday😌); so most have their renewable power source on-site, mostly diesel generators.
    
6. #### Microwave dish
    
    In some locations, such as remote rural areas, a microwave satellite dish is used instead of fiber optic cables to act as a transmission to connect the mast to the rest of the masts on the network. To do so, the dish must be within line of sight of a dish on another mast.
    

The article from Vodafone is [here](https://www.vodafone.co.uk/newscentre/smart-living/everything-you-need-to-know-about/mobile-phone-masts-everything-you-need-to-know/).

### **How are Phone Calls Connected**?

To answer this, first, you should know that your phone is almost always connected to the nearest network mast with the strongest network signal, depending on the network provider. It is why you have those small network bar(s) at the top of your phone, it shows how close you are to the mast and how strong the signal is. If you are in an area where your phone or device can't reach a network mast from your internet service provider, you get the 'No Signal' or 'No Network' message.

Also, every network mast out there is connected to the next mast, either via cables or radio signals(wirelessly). You might not see it, but they are all talking to each other over long distances.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680809951556/587cc6e8-e269-452e-aef1-3d83710256ad.jpeg align="center")

Back to the main question, how do calls go from one edge of the country to the other side? The very simple answer is that your call jumps from one mast to another till it reaches the person you're calling. If you are making a call from Abuja to someone in Lagos, for both you and the caller, your calls follow through all the masts between you and the individual. Your service providers like MTN, do something called routing, to make sure that the calls pass through the most efficient masts while this call is ongoing. Efficiency can be in the sense of making sure calls pass through masts that have lesser calls going through them at that moment, making sure calls take the shortest distance, avoiding faulty masts, etcetera.

For a little more technical on how calls move, let's talk about the process:

* **Initiating the Call:** When you start a call, your phone sends a radio signal to the nearest network mast it is connected to. The mast picks up the signal and sends it to the nearest base station.
    
* **Authentication:** The base station ensures your phone is allowed on the network, by checking the sim card, it then assigns it a frequency channel and a time slot.
    
* **Call Routing:** The base station sends the call to the mobile switching center (MSC), which is responsible for routing the call to its destination.
    
    For example, MTN has numerous Mobile Switching Centers across the country, these control centers receive calls from the base station your mast sent, find where the person the call is meant to get to is in the country, and how many masts to get to the nearest base station for that person, it then sends the call in that direction.
    
* **Mast Routing:** In this case, there are two main scenarios, one is if the individual being called is within the same mast range as the caller, then the call doesn't have to leave that mast, if not, the call hops from one mast to another as the MSC directs.
    
* **Voice Quality:** The quality of the call is dependent on factors like signal strength, interference, and distance. If the signal is weak, the voice quality may be poor or the call may be dropped.
    
* **Call Termination:** When the call is over, your phone sends a signal to the network indicating that the call has ended. The network releases the frequency channel and time slot assigned to your phone.
    

This all happens when you make a call from one phone number to another, it's also almost the same thing that happens when you send text messages too, SMS(Short Message Service) with some underlying protocol difference though. For Internet connection, it's also almost the same, but with some interesting touch of complexity, let's hop on those fun parts.

### How you access the Internet with just a SIM and Network Masts

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680845784600/7c4883da-060d-4443-b82b-ce548e9d3578.png align="center")

Every time we use mobile data, that's internet access from your mobile phone through the SIM(Subscriber Identity Module) provided by ISPs like MTN, Airtel and the like in Nigeria, some radio magic happens.

When you or anybody access the internet, it simply means you have access to files on the **IN**terconnected **NET**work, a connection of millions of computers around the world. This means you can reach and talk to computers owned by Google, therefore allowing you access to applications on their computers like Google, the search engine, Youtube, their Video sharing platform, not just Google's computers, TikTok, Linkedin, Facebook, Amazon, Jumia, Bolt and every other website you can reach out there, you can reach these applications because they are on the internet. You also have the ability to send files to computers on the internet(UPLOAD) or pull down files from the internet(DOWNLOAD)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680858690329/b51dfd8b-080c-4989-bfeb-3d2c0d284bd3.png align="center")

⬆️ | [Image](https://www.submarinecablemap.com/) showing the Fiber cables under the sea, powering the internet.

How you reach those servers is in itself a giant networking topic and a complex feat of engineering handled by Internet service providers around the world. But we'll just talk about the role the network masts play in the whole process.

* When you access the internet(assuming you still have an active data **subscription🥴**), the data(usually a type of request), is transmitted from your phone to the nearest network mast it is connected to, in the form of radio waves.
    
* The data is then processed by the radio unit(I talked about radio units earlier up) on the network mast, which converts the data from digital to analog signals that can be transmitted over airwaves.
    
* The data is then transmitted to other network masts and base stations which serve as a gateway to the ISP's core network.
    
    The core network is typically made up of multiple interconnected data centers and high-performance equipment and infrastructures that are designed to handle large volumes of data traffic, responsible for managing the routing of data traffic within and between networks.
    
* The data is routed through the ISP's core network to an internet gateway( a component that connects the ISP's network to the internet).
    
* The internet gateway sends the data out onto the internet, where it reaches the destination server for the requested data, most likely across the world.
    
* The data travels back through the ISP's core network and is routed to the appropriate base station and network mast to reach the user's device.
    
* Your phone receives the requested data. This entire process occurs within a matter of seconds.
    

To make this quite relatable and practical, we'd use Whatsapp. Let's try a scenario where we download a voice note(an audio file) from a friend using MTN's network

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680864492972/23e870af-4f7b-4068-803f-07b3d982b1db.png align="center")

➡️ | You open Whatsapp, and you get to the DM where you received the voice note from the friend.

➡️ | You tap the download icon, and then WhatsApp sends a data request to the network mast your phone is connected to, either MTN, Airtel or GLO or any other ISP around the world, in this case, MTN. This request is transmitted as radio waves over the air from your phone to the network mast.

➡️ | The network mast receives the request and forwards it to the nearest base station, which serves as a gateway to the MTN's core network.

➡️ | The request is then transmitted across the MTN core network to an internet gateway, which connects the MTN network to the outer internet.

➡️ | The internet gateway sends the request out onto the internet, where it reaches a WhatsApp server, these servers are located in data centers across the world, in places like the United States, Europe, and Asia. So depending on which server the picture is on, the request would most likely pass through fiber cables under the sea to get the picture.

➡️ | WhatsApp server gets the voice note you asked for and sends it back through the internet to MTN's network.

➡️ | The voice note travels back through the MTN's core network and is routed to the appropriate base station and network mast to reach your phone.

➡️ | Your phone receives the voice note and stores it in memory or storage, allowing you to download and listen to it.

This happens for everything you download onto your phone, images, videos, audio, stickers, even voice notes, voice and video calls on WhatsApp, and just almost anything from any app or website you see on your device using an internet connection, that you didn't previously have stored in memory or storage. The best is that it happens so fast, you don't even know what just happened.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680862622916/2caeff0c-3047-4ab2-817d-c01461e4df12.jpeg align="center")

So, yeah, without network masts, the majority of everyone wouldn't almost be able to do anything, make calls, send texts or use the internet. This is slowly changing though, as there are already things like FTTH(Fiber-To-The-Home) where you have a wired connection to the internet instead, there is also the battle of satellite internet with the likes of Starlink starting the parties and companies like OneWeb also Joining in. Also, we have our old and popular friend Wifi/Hotspot networks too.

**Then why do we pay for internet I still hear you ask?**

If you didn't figure out that yet, yeah, let's talk about it. Earlier on we talked about network masts, first, those things are expensive to set up, getting a piece of land to set them on, the structure and the work to get them up, the cost of the antennas, radio unit, the cost of a backhaul if it is used(having to dig the ground and lay cables to connect one mast to another), cost of cables, costs of generators, the cost of fueling, they need to put someone on salary to constantly monitor the premise. While writing this article, I came across news article where guys randomly walk into a network mast premise, steal diesel, and use the proceed from the crime sales to buy pepper soup to calm down for the evening, and that's just on the light side of the vandalism, it gets worse. They also have to pay engineers to manage the hardware and software sides of everything. Add that all up and multiply it across all the network masts you see around and you can very quickly see how cost runs.

One other thing, companies like MTN don't also connect directly into the internet, they have to connect to other ISPs for service, it's a hierarchical order of connection, and there are tiers to this:

**Tier-1:** these are the largest and most interconnected networks in the world. They have direct connections to all other Tier 1 ISPs, as well as to many smaller ISPs and content providers.

**Tier-2:** there are smaller networks that connect to Tier 1 ISPs and other Tier 2 networks. They typically serve a regional or national market, and may also provide services to smaller ISPs or businesses.

**Tier-3:** these are local or regional networks that connect to Tier 1 or Tier 2 ISPs to access the wider internet. They may provide services to residential or business customers or may serve as backhaul providers for smaller ISPs.

In the case of MTN in Nigeria, it is regarded as being on a Tier-1 ,based on its deep network coverage and infrastructural size, it is in the same space as Globacom and Airtel, but on the global scale, MTN still needs to reach out to other ISPs to pull data off, they pay to do so too. So yeah, asides staff salary and profits, there is a lot of running cost. You should now see why getting free internet isn't sustainable.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680864966845/442d0907-38b9-4537-8071-ba6084828b46.gif align="center")

If you read to this point, thank you..💪🏾..

It feels like a very long one, but it was fun writing this, thanks for your time, I hope you picked something.

> And you, yeah you, if you're seeing this, hmmm. It's .......