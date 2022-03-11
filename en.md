---
layout: single
permalink: /en/
title: "Satellite Communication Threats"
excerpt: "English"
last_modified_at: 2022-03-10T10:23:16-04:00
toc: true
toc_sticky: true

header:
  overlay_color: "#005"
  overlay_filter: "0.5"
  overlay_image: /assets/images/spacex-VBNb52J8Trk-unsplash.jpg
  caption: "Photo by [SpaceX](https://unsplash.com/@spacex)"
excerpt: "This is an adversary-neutral review of known risks when using Satellite communication tools such as satphones, BGANs, and even LEO-orbit (e.g. StarLink) terminals."
---

This document is a **public draft** and is still under review. <br /><br />**Please offer [feedback](/contact) if you have any**. While the author has focused primarily on summarizing existing, known, historical risks of satellite communications, the mitigations suggested may be incomplete. Consider your specific needs, vulnerabilties, and your adversary in applying this document to your situation.
{: .notice--danger}

# Overview

Satellite Communications tools provide critical access during complete
Internet shutdowns and are difficult -- but not impossible -- to block.
However, the risks of using these tools must be considered. Satellite
devices are easy to geolocate, with documented evidence of this turning
into lethal actions, but the communications can be intercepted, jammed,
and users being arrested/harassed because of the hard-to-conceal use of
specialty hardware are worth consideration.

# Goals

Satellite communication tools provide unique, unmatched qualities when
dealing with remote locations, emergency situations, fluid conflict
zones, and as a final recourse against Internet shutdowns. However, they
are subject to their own specific risks which are impossible to fully
mitigate.

It should be presumed that sat phone conversations/messages are not
private without additional tools, and that usage of satellite
communications can be used to locate the device, particularly when
active for long periods of time. The requirements for an adversary to do
these are not significant, but do require focused effort and will to do
so.

The commercial, end-user landscape of these tools is full of expensive
hardware, cost-prohibitive connectivity costs, legal and import/export
restrictions -- and a steep learning curve around the intentionally
obfuscated safety and security of the usage of the products.

This document will attempt to map out the known vulnerabilities of
satellite communications, as well as how those and other concerns
contribute to the risks journalists, human rights defenders, and others
face when using them.

This does not take into account any specific adversary but tries to
identify the complexity of the different threats and how much resources,
capacity, and/or will/intent an adversary would need to use the threat.

"[S]atellite phones may also be susceptible to jamming, surveillance, interception, and other security threats. In 2012 and 2017, researchers identified weaknesses and cracked satellite phone encryption standards used by multiple service providers, underscoring that users should have no expectation of privacy when communicating by satellite phone. Additionally, satellite phone users could potentially be tracked through frequency emissions, commercially available tracking devices, and built-in global positioning system (GPS) capabilities. While GPS features may facilitate locating an individual in an emergency situation, it could also be a potential security vulnerability to be exploited and used for malicious intent, like kidnapping or detention. […] It is also feasible for a nation-state or criminal enterprise, with financial resources and access to the right commercially available technology, to track a satellite phone and intercept communication beyond voice calls and texts." – OSAC Guide for Overseas Satellite Phone Usage 7/2/2021
{: .notice}

## Scope

This is focused on 2-way satellite communications devices, including sat
phones, VSAT terminals, and Starlink. Some of the risks discussed may
also apply to receive-only / broadcast satellite in situations where
satellite dishes are regulated/illegal.

This document is focused on Internet shutdown, crisis, conflict, and
emergency situations where a journalist, activist, or human rights
defender may be using these tools to access and share information
despite adversaries ranging from their own government's law enforcement
to organized militias and even to State-backed militaries.

Risks are inherent in using any form of communication tool when speaking
truth to power. Satellite communication tools are often rolled out
quickly during crises as they solve many core communication challenges.
This document's goal is to also share the risks that come with satellite
communications, as they are often not well understood.

### A note on Alternative Communication Options

While not in scope for this document, for situations such as preparation
for internet and/or electricity shutdowns, planning for multiple
alternative communication options adds resilience and enables more
flexibility during a crisis. Topics, plans, and tools can include:

-   Planning for physical meetings (and contingency planning if there
   are safety concerns or limited movement options)
-   HF/VHF Radio
-   Shortwave receivers to track international news

***Note**: Contributions to supplement this guide with detailed
documentation on the operational and legal considerations of the above
would be welcomed.*
{: .notice--info}

# Glossary of terms

-   **"Bent Pipe"** - a term used to discuss "how" satellites deal with communication -- for the most part, the satellite simply relays the signals it receives directly between the device and the groundstation.
-   **BGAN** - Broadband Global Area Network - Inmarsat's satellite internet and related hardware
-   **Downlink** - the broadcast from the satellite in orbit back down. Generally the "footprint" of these cover wide areas (hundreds of miles) each.
-   **ELINT** - A subset of SIGINT ("SIGnals INTelligence"), [ELINT ("ELectronic INTelligence")](https://en.wikipedia.org/wiki/Signals_intelligence#ELINT_and_ESM) focuses on only the radio frequency and related electronic components of communication, to support geolocation, signal jamming, and interception needs. A common term in researching satellite communication security.
-   **GEO** - [Geostationary orbit](https://en.wikipedia.org/wiki/Geostationary_orbit) ("Geosynchronous Earth Orbit") - a satellite, often for communications, which is in an orbit such that it is always in the same location in the sky above a fixed point on the Earth's equator. These are high orbits, so there is additional latency in communications.
-   **Groundstation** Also referred to as a "teleport", Earth Stations, and [Satellite Earth Stations ("SES")](https://en.wikipedia.org/wiki/Ground_station)) - Satellites relay the comms to dedicated ground stations where the data/call rejoins the "normal" terrestrial internet. Groundstations are strategically located for satellite visibility, but may be in countries without strong human rights or data privacy track records. ***Ground Stations can also refer to any two-way satellite communications terminal on the ground.***
-   **LEO** - [Low Earth Orbit](https://en.wikipedia.org/wiki/Low_Earth_orbit) - Due to their lower orbit, satellites in LEO offer higher bandwidth and lower latency, but require more satellites to cover a communication area.  Iridium and Starlink are examples of LEO communications satellite systems.
-   **Satphone** / **handset** -- a device in the form factor of a large cell phone with a non-directional antenna.
-   **Uplink** - the communication from the satellite device up to the satellite in orbit. Directional antennas (dishes) limit the area one must be to intercept this, but most sat phones do not have directional antennas.
-   **VSAT** - "[Very-small-aperture terminal](https://en.wikipedia.org/wiki/Very-small-aperture_terminal)" - a two-way groundstation with a dish antenna smaller than 3.8 meters (so most satellite internet antenna like for starlink). These tend to require some "aiming" to make a connection.
{: .notice}

# Commonly overlooked challenges

Most of this document focuses on the operational security challenges and
mitigations involved in using satellite communications. However, there
are some baseline requirements to also keep in mind to simply ensure the
service is available when and if you choose to use it.

## Electricity

All satellite comms devices require power, just like normal routers and
phones. Dishes and BGAN style terminals require anywhere from 20 to 100
watts while actively transmitting, which can rapidly exhaust a battery
backup / UPS system. Satellite phones come with batteries capable of up
to 3 hours active time and 30 hours idle.

### Mitigations:
-   Make sure your satphone is fully charged, re-charging when power is available.
-   Maintain backup batteries, and ensure USB chargers are compatible
    with your satphone and that they are fully charged.
-   Have (and test) a plan for usage of satellite terminals and base
    stations, and how they can be powered if electricity goes out. Know
    how long your backup solutions (generator, battery, solar) can last,
    and under what conditions.
-   Identify what other devices will also need power (possibly drawing
    from the same backup sources) such as network routers, laptops,
    computers/servers without built-in batteries \-- to make sure the
    satellite connection will be functional for your needs.
-   Do you have adapter power cables for these devices which could be
    powered from a vehicle?

## Service Subscription and Costs

Satellite data plans are expensive and often tightly constrained in
terms of total or daily/monthly usage. This is not a limitation you want
to be concerned about during a crisis, so ensuring there is someone or a
process supporting account maintenance is valuable.

### Mitigations:
-   Minimize use of satellite communications when other options are available.
-   Ensure your SIM card is topped up as early as possible.
-   Know how your plan works if you reach your usage limit: will it stop
    working until you manually add funds? Will it continue at lower
    rates? Will it continue and charge overage fees?
-   Have a person outside of the conflict who has the information needed
    to track usage and recharge the SIM if the conflict is extended, or
    if you are unable to continue funding it directly (this could be due
    to other issues such as banking problems, or
    over-compliance/confusion around sanctions). This can protect
    against loss of access leading to an inability to regain access.

<!--
# Summary of Mitigations to consider

    -   *(To be summarized from below at final doc stage)*
-->

# Risks and Mitigations

## Device Legality and Seizure

Satellite communication tools, from phones to more robust data
connection setups, are often tightly regulated or outright illegal.
OSAC's July 2021 report here:
<https://www.osac.gov/Content/Report/9db45731-1eec-477a-a7af-1bf950cb4013>
has a list of countries where sat phones are known to be illegal.
Additional law tracking resources include UNIDIR's Cyber Policy Portal
(<https://unidir.org/cpp/en>), GPD's Encryption Policy map
(<https://www.gp-digital.org/world-map-of-encryption/>) , and
<https://cyrilla.org/>

In addition, due to the need for an outside, direct line of sight to the
sky - combined with visually distinct features from cell phones and
other equipment, sat phones and devices are difficult to conceal. Device
seizure (and the further impacts that can have) is a very real risk to
consider. Devices can reveal your contact network, stored files, and
recent call logs, as well as be used potentially to impersonate you to
your contacts.

Further, given the illegality of non-registered devices in many
countries, possession/use alone can be enough to detain someone.

### Mitigations

-   Regularly purge contacts, recent calls/message and any other
    content/documents on the device. Minimize app usage and use
    automatically disappearing messages options. Log out of
    apps/websites.

-   Conceal the phone/antenna/dish and use a bluetooth headset or wifi
    router to not be obviously in possession of the device when you use
    it. Different materials will have different effects if covering a
    satellite dish. In general, any covering is likely to reduce your
    signal, so consider non-metallic paint or light, dry cloth (water --
    in clouds, rain, and even trees is a significant factor in signal
    strength). Also consider your adversary -- are you trying to conceal
    this from someone walking by on the street, or from someone flying
    over in a helicopter? Both?

-   When purchasing, seek out dual-use equipment, for example, devices
    which look like GPS units but which also provide a satellite data
    connection. If using this approach, ensure that users have a reason
    to use a GPS device and familiarity with its features.

-   If you are in a location where raids or similar physical searches
    are likely, find a safer location to store equipment, and carefully
    consider the potential value of the satellite device against the
    possibility of arrest. Should you dispose of or destroy this device
    instead?

### Details

"OSAC members have reported difficulties importing satellite phones in countries where the devices are technically permitted (or not restricted). In Libya, there are no laws against satellite phones, but there have been multiple reports of authorities confiscating satellite phones, GPS devices, and personal tracking devices at the airport. " -- [OSAC Guide for Overseas Satellite Phone Usage](https://www.osac.gov/Content/Report/9db45731-1eec-477a-a7af-1bf950cb4013) 7/2/2021 (**Also has a table of known laws**)
{: .notice}

## Device Geolocation

Multiple approaches can be used to geolocate an active device. Most
require proximity, specific technology, and some skills, so are
generally limited to dedicated adversaries, but all of these approaches
have options where one can trade cost for expertise (e.g. easy to use
but expensive commercial/off-the-shelf tools vs easy-to-source, vs
low-cost DIY tools with a steep learning curve). There is a large market
for off-the-shelf commercial tools that are available for this,
primarily to support frequency usage / regulation activities. These
tools can include fixed antenna, vehicle-mounted and/or movable antenna,
as well as aerial drone-mounted and handheld hardware.

Military adversaries in a conflict zone are likely to be resourced with
skills and devices and also likely to be actively scanning for satellite
communications.

Government-level legal pressure/demands of relevant service providers
provide yet another avenue for this information.

### Mitigations

-   Also practice the mitigations under device seizure, above.

    -   In specific, the use of a wireless router to give physical
        distance from the satellite device provides specific benefit
        here by giving you some warning of a raid against the location
        of the device, as well as (in military/conflict situations) some
        distance from kinetic attacks such as missiles or other
        bombardment.

-   Leave the device turned off when not in use

-   Change location of where you call from (but do not move while using
    the device if avoidable)

-   Don't use at home/work locations except in emergency

-   Minimize usage time

-   Consider the terrain / urban infrastructure and how it can help
    limit geolocation. In Afghanistan for instance, it's extremely
    difficult to use DF equipment due to the mountains and deep valleys,
    which act as an automatic shield for signals.

**Additional Mitigations (Law Enforcement type adversary)**

Making sat-phone calls from highly populated areas can make it difficult
for authorities to identify and physically intercept the caller after a
short call.

**Additional Mitigations (State/Military type adversary)**

Using devices in locations far from urban areas, government
infrastructure, military installation/activity, and borders, and using
them for short periods of time and from different locations each time
provide additional mitigations against direction finding equipment.

### Details

**Using Radio Frequency Triangulation**

Satellite phones are the highest risk here due to their omni-directional
antenna setup. As differentiated from devices which use large satellite
dish-style, directed antennas, Sat Phones are the easiest for an
adversary to geolocate due to their use of L band comms with an
omni-dorectional antenna. The band is a commonly monitored band, and the
omni-directional antenna means it has significant "spill-over" of RF
noise visible to direction finder devices. This risk is higher when the
phone is used or even left turned on for a long time. Even if not "used"
but only tuned on, the phone will send frequent pings to the satellite
which could be tracked for triangulation.

"\[Satellite communications\] can be triangulated with affordable, even homemade tools. […] Highly developed countries with advanced technical security are likely to have this capacity, less developed states and even non-state actors may be able to develop the capacity."  -- SMALL WORLD NEWS GUIDE TO SAFELY USING SAT PHONES 3/2012
{: .notice}

“whoever is important enough to have a \[satellite\] terminal is important enough to bomb.” - Collin Anderson, Twitter 2022
{: .notice}

"It is possible that the Syrian army used the long-established ‘direction-finding’ approach to pin-point the location of the journalists in the media centre. […] It is relatively simple to receive this signal for a trained technician, using an RF spectrum analyser. […] After detecting the presence of sat phone transmissions, it would be relatively easy for communications technicians to find the location of the phone by tuning to that frequency, moving the antennas to find the direction where the signal was strongest and then triangulating with their opposites. This would provide an ever-shrinking triangle until the points intersect." -- SaferMobile Be Afraid, Be Very Afraid of Satellite Phones in Insecure Locations Anonymous, 2/23/2012
{: .notice}

“Russia has spent a long time perfecting these techniques. On April 21, 1996, Chechnya’s breakaway president, Dzhokhar Dudayev, was speaking on a satellite phone with Russian envoy Konstantin Borovoi about setting peace talks with Yeltsin. During the phone call, he was killed by a signal-guided missile fired from a Russian jet fighter. The warplane had received Dudayev’s coordinates from a Russian ELINT (electronic intelligence) plane that had picked up and locked on to the signal emitted by the satellite phone. It was Russian deception and brutality at its finest. -- Foreign Policy, Kill The Messenger, Robert Young Pelton, March 3, 2012
{: .notice}

**Intercepting GPS Coordinates**

Any adversary capable of intercepting (see below) also has the potential
to receive precise GPS coordinates. These are in some cases transmitted
in the clear, and can be therefore discovered by capturing uplink and in
some cases much more widely available downlink signals as well.

"It is very likely that the GPS location data is transmitted by the sat phone is sent in the clear.  According to the specification (GSM-1 04.008 Section 10.1.8) the message from the sat phone requesting a channel carries among other information the dialed number and the GPS location data before the handset identity is established.  This makes the location data easily readable by an adversary." – SaferMobile Be Afraid, Be Very Afraid of Satellite Phones in Insecure Locations Anonymous, 2/23/2012
{: .notice}

**Legal pathways**

In addition to technical means, there are also legal avenues (simply
demanding records from satellite service providers directly and/or in
the country(s) where their ground stations are located.

"There are a few different ways by which satellite phones can be tracked.  The first—and easiest for a government actor—would be to simply ask or pressure a company to hand over user data."  -- https://www.eff.org/deeplinks/2012/02/sat phones-syria-and-surveillance
{: .notice}

## Communication Interception

Similarly to the device geo-location options, interception of satellite
comms has a range of technical options as well as legal pathways. Sadly,
research to date has revealed that the baseline security of the
communication is not a priority for providers or the standards-setting
bodies.

"Modern satellite phones encrypt voice traffic to prevent eavesdropping. It's that modern GMR-2 algorithm that was the focus of the research, given that it's used in most satellite phones today. […] The end result was that encrypted data could be cracked in a fraction of a second. "This again demonstrates that there exists serious security flaws in the GMR-2 cipher, and it is crucial for service providers to upgrade the cryptographic modules of the system in order to provide confidential communication," said the researchers." -- ZDNet New attack can now decrypt satellite phone calls in “real time” 7/6/2017
{: .notice}

More on the 2012 attack from a cryptanalysis/standard viewpoint :

"[E]avesdropping on satellite communications is (in principle) easier than eavesdropping on cellular signals. That’s because satellite ‘spot beams’ cover relatively broad geographic territories (Thuraya’s are 600km on average). So you don’t just have to worry about eavesdropping by your neighbor, you have to worry about eavesdropping by neighboring countries." -- Satellite phone encryption is terrible. Anyone surprised? 2/5/2012
{: .notice}

### Mitigations

-   Because Sat Phones don't operate well as "standby", but a set
    schedule of when you call is risky, decide on a method to plan call
    times
-   Using secure Internet communications tools on top of a data
    connection provides security against interception of the message
    content (at higher financial cost). This includes both end-to-end
    encrypted apps like Signal, but also more simple encrypted-to-server
    communication tools like webmail and video conferencing platforms.
-   Presume that an adversary with specific interest can and will be
    able to track and often listen in to comms, so focus usage of the
    satellite communication options for emergencies, public data, or
    urgent sharing of information (e.g. video documentation relevant to
    a human rights case and/or of key journalistic importance) with the
    understanding that an adversary may also see this and leverage it.

### Details

**Uplink/Downlink Interception**

"Proximity is relative. First you have to distinguish between what's commonly called "tactical" intercepts which are done in the field. For those, you receive the phone uplink but a phone transmits with quite a bit of power and doesn't have very directional antenna, so it can be several kilometers, especially if you have a good vantage point.  Then there is what's called "strategic" interception setups, done at dedicated facilities. What goes up must come down and most satellites are just "bent pipe", dumbly retransmitting what they receive back to earth. So instead of receiving the phone, you can just listen to the sat retransmitting the phone comms back to the ground station."  -- Sylvain (paraphrased)
{: .notice}

“As the conflict grew, an increasing number of users migrated from Thuraya to other networks, both because of the interruptions associated with the intermittent jamming as well as a strong perception among many in the Libyan opposition that the Thuraya servers were especially vulnerable to LAJ signals intelligence or some other form of unspecified interception. […] It would become clear after the conflict ended that this concern was at least in part well-founded: the LAJ was found to have training materials for the L3 Communications Tactical Thuraya Monitoring System, an interception and localization package developed for field-deployed signals intelligence applications.”  --  Revolutionary Risks: Cyber Technology and Threats in the 2011 Libyan Revolution , John Scott-Railton, U.S. Naval War College Digital Commons / CIWAG Case Studies
{: .notice}

“By this point, the regime's electronic warfare had become even more sophisticated. Cell phone and landline calls had long been monitored, but now the spies turned their attention to satellite phones. To avoid NATO air strikes, one team of Ukrainian mercenaries set up shop in a kindergarten, right around the corner from the intelligence headquarters; from there they snooped on sat-phone traffic using frequency scanners. Gadhafi had declared that anyone caught with a satellite phone could be sentenced to death.” -- Jamming Tripoli, Matthieu Aikins, Wired, May 18, 2012
{: .notice}

**In-orbit Interception**

A very small number of nations have the potential ability to position satellites alongside (“co-orbital”) popular communication satellites to eavesdrop on communications to/from that satellite. This is very rare and much more likely focused on military/defense outcomes, but is in the realm of possible:

"That new primary mission was “Thuraya collection and Afghanistan/Pakistan exfiltration.” The first confirms that the close placement near, and apparent co-orbital shadowing of, the commercial Thuraya 2 satellite is indeed intentional: Mentor 4 is indeed eavesdropping on Thuraya 2. The second relates to a more typical mission of ORION SIGINT satellites: collecting radio signals from a wide geographic region on Earth. The document also mentions (in the byline with the illustration) that the satellite was expected to be fully operational around mid-May of 2009. This tallies with the observed moment of Mentor 4’s arrival near 44 degrees east. It arrived there in late April of 2009, although it did not fully stabilize there until July 2009 (see diagram below.) Like PAN’s orbital behavior, the behaviour of Mentor 4 is unusual for a SIGINT satellite. The very close placement and closely synchronized co-orbital movement of Mentor 4 with regard to Thuraya 2 is unique, in the sense that it is behavior different from both earlier and later satellites in the ORION series: none of these shadow another satellite this closely. " -- https://www.thespacereview.com/article/3095/1
{: .notice}

In a speech outlining France’s space policy and security issues, Parly said that the Athena-Fidus satellite, operated jointly by France and Italy, was approached “a bit too closely” by Russia’s Luch-Olymp craft, known for its advanced listening capacity. “It got so close that we might have imagined it was trying to intercept our communications,” she added. “Trying to listen to your neighbours is not only unfriendly, it’s an act of espionage.” -- https://www.theguardian.com/world/2018/sep/07/france-accuses-russia-spying-satellite-communications-espionage
{: .notice}

**Groundstation Monitoring**

"Governments can also intercept communications on satellite phones. Satellite phone calls with a mobile phone or landline are routed through ground stations in numerous countries. When transmitting through these ground stations, communications providers must comply with local legal and regulatory frameworks, making it possible for local governments to intercept private communications. " – OSAC Guide for Overseas Satellite Phone Usage 7/2/2021
{: .notice}

Last week’s news that China has installed a ground station for intercepting signals transmitted through the US and Russian communication satellite systems makes one wonder just how proof against interception and interruption are satellite communication systems. Unauthorized listening-in would seem to be unavoidable because the geostationary and near-geostationary satellites of the military and civilian systems radiate signals in all directions and these signals can be picked up by any ground station over nearly one-third of the Earth’s surface from which the satellite can be seen. -- https://www.newscientist.com/article/dn10536-china-can-eavesdrop-on-us-satellites/
{: .notice}

## Jamming

Jamming is used to block all communications in an area (downlink) or
with a specific satellite (uplink). Both are relatively easy and
inexpensive, but untargeted. Jamming a satellite (uplink) can have
international impacts and would be a breach of ITU's [Article
15](https://www.itu.int/en/ITU-R/terrestrial/tpr/Documents/Article15-RR16.pdf),
Interference from Radio Stations.

### Mitigation

-   Downlink jamming must be within line of sight,
    moving to a different area could get outside of the area of effect.
    Consider if your adversary is trying to force you to move.

### Details

"There are two main types of satellite jamming. The first, uplink jamming, interferes with the signal going from a ground station or user terminal to the satellite. An RF signal of the same frequency as the targeted uplink signal is transmitted to the satellite, aiming to limit the satellite transponder from differentiating between the jamming signal and the actual signal. The second type, downlink jamming, disrupts transmissions sent from the satellite to ground-based or airborne receivers using RF signals that mimic the frequency of the downlink signal. It aims to inhibit ground users from receiving transmissions from the satellite and only needs to be as strong as the signal being received on the ground. Uplink jamming is considered more difficult because greater transmitter power is required to reach a given satellite’s transponders. It could be more impactful, however, due to its ability to degrade the satellite’s signal for all its users. Because downlink jammers must be within the field of view of the receiving terminal’s antenna, however, the effects of downlink jamming are more localized." -- https://ontheradar.csis.org/issue-briefs/satellite-jamming/
{: .notice}

"Jamming technology tends to be commercially available and relatively inexpensive. Satellite jamming systems are easy for states and non-state actors to develop given the relative low cost of their procurement and operation. There is a low threshold of technological competency required to perform jamming, and the technology is available to a plethora of actors across the globe. For example, interference with satellite signals has emanated from Indonesia, Cuba, Ethiopia, Libya, and Syria, among others." -- https://ontheradar.csis.org/issue-briefs/satellite-jamming/
{: .notice}

“It is true that the Starlink ground terminals will be broadcasting, and thus potentially targetable using RF signal detection equipment. But I doubt they’d be that high of a priority for Russian targeting, so I think the odds of them being targeted is probably low,” Weeden said Monday by email. “A much bigger challenge would be Russian ground-based mobile jamming, which is sophisticated and can already deal with existing satellite signals such as GPS and satellite communications.” -- SpaceX heeds Ukraine’s Starlink SOS
{: .notice}

“Over the weekend of February 19, transmissions from two television satellites that served a wide range of news programming to Libya and the region were disrupted by jamming, according to the Lebanese Telecommunications Regulatory Authority.31 And on February 21, Al Jazeera accused Libya of jamming its satellite transmissions in the region, and stated that it had conclusively identified the jamming as emanating from an LAJ intelligence services building south of Tripoli.
Satellite telecommunications were not immune to LAJ disruption and denial efforts, which were likely targeted against the use of satellite telephones like the Thuraya handset, which were widely used in Libya. On February 25, Thuraya accused Libya of having engaged in a week’s worth of jamming of the Thuraya-2 satellite that provided satellite phone and data connectivity to Thuraya devices within Libya.33 Shortly thereafter, Thuraya announced that its technical efforts had restored voice services to much of Libya. Nevertheless, users of Thuraya phones continued to experience substantial difficulty connecting throughout the revolution.”  -- Revolutionary Risks: Cyber Technology and Threats in the 2011 Libyan Revolution , John Scott-Railton, U.S. Naval War College Digital Commons / CIWAG Case Studies
{: .notice}

"Jamming can also occur accidentally: in 2015, U.S. military officials noted they were unintentionally jamming satellite communications an average of 23 times per month. Purposeful jamming can be difficult to differentiate from accidental interference, making attribution more challenging." -- Satellite Jamming https://ontheradar.csis.org/issue-briefs/satellite-jamming/ CSIS
{: .notice}


Device Software Security
------------------------

#### Mitigation

-   To the extent possible, leverage satellite communications devices as
    untrusted network connections and layer on independent security.

#### Details

"Between October and December last year, researchers from IOActive analyzed the firmware of popular satellite communications (SATCOM) devices that are used in the military, aerospace, maritime, critical infrastructure and other sectors. The research covered products manufactured or marketed by Harris, Hughes Network Systems, Cobham, Thuraya Telecommunications, Japan Radio Company (JRC) and Iridium Communications. The analysis focused on SATCOM terminals that are used on ground, in the air and at sea, not satellite communications equipment in space. "IOActive found that all devices within the scope of this research could be abused by a malicious actor," the IOActive researchers said in a report published Thursday. "We uncovered what would appear to be multiple backdoors, hardcoded credentials, undocumented and/or insecure protocols, and weak encryption algorithms." -- Satellite communication systems rife with security flaws, vulnerable to remote hacks 4/18/2014
{: .notice}

"Unfortunately, except for Iridium, the vendors did not engage in addressing this situation," the researchers said. "They did not respond to a series of requests sent by the CERT Coordination Center and/or its partners." -- https://ioactive.com/pdfs/IOActive_SATCOM_Security_WhitePaper.pdf
{: .notice}
