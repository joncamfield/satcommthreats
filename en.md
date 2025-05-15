---
layout: single
permalink: /en/
title: "Satellite Communication Threats"
excerpt: "English"
last_modified_at: 2023-11-15T21:36:16-05:00
toc: true
toc_sticky: true

header:
  overlay_color: "#005"
  overlay_filter: "0.5"
  overlay_image: /assets/images/spacex-VBNb52J8Trk-unsplash.jpg
  caption: "Photo by [SpaceX](https://unsplash.com/@spacex)"
excerpt: "This is an adversary-neutral review of known risks when using Satellite communication tools such as satphones, BGANs, and even LEO-orbit (e.g. StarLink) terminals."
---
**Please offer [feedback](/contact) if you have any**. While the authors have focused primarily on summarizing existing, known risks of satellite communications, the mitigations suggested may be incomplete. Consider your specific needs, vulnerabilities, and your adversary in applying this document to your situation.
{: .notice--danger}

# Introduction

Risks are inherent in using any form of communication tool when speaking truth to power. Satellite communication tools are often rolled out quickly during crises as they provide critical access and are difficult -- but not impossible -- to block. However, the risks of using these tools must be considered.

This guide discusses threats which are widely applicable to 2-way satellite communications devices, such as satellite phones and pagers, Inmarsat BGANs, Starlinks, and VSAT terminals. Some of the risks discussed may also apply to receive-only / broadcast satellite in situations where satellite dishes are regulated/illegal. These satellite devices are easy to geolocate, with documented evidence of this turning into lethal actions. The communications can also be easily intercepted, jammed, and users can be arrested/harassed because of the hard-to-conceal use of specialty hardware.

"[S]atellite phones may also be **susceptible to jamming, surveillance, interception, and other security threats** \[…\] users should have **no expectation of privacy** when communicating by satellite phone. Additionally, satellite phone users could potentially be **tracked through frequency emissions, commercially available tracking devices, and built-in global positioning system (GPS) capabilities**. \[GPS\] could also be a potential security vulnerability to be exploited and used for malicious intent, like kidnapping or detention. \[…\] It is also feasible for a nation-state or criminal enterprise, with financial resources and access to the right commercially available technology, to track a satellite phone and intercept communication beyond voice calls and texts."<br />--*OSAC Cybersecurity Team (July 2 2021) [Guide for Overseas Satellite Phone Usage](https://www.osac.gov/Content/Report/9db45731-1eec-477a-a7af-1bf950cb4013) OSAC.gov.*
{: .notice}


<!--This document will attempt to map out the known vulnerabilities of
satellite communications, as well as how those and other concerns
contribute to the risks journalists, human rights defenders, and others
face when using them.-->

This document is focused on Internet shutdown, crisis, conflict, and emergency situations where a journalist, activist, or human rights defender may be using these tools to access and share critical information, with a wide range of adversaries including well-resourced, state or military-level ones.

This does not focus on any specific adversary but tries to
identify the complexity of the different threats and what resources,
capacity, and intent an adversary would need to use the threat.

<!--Satellite communication tools provide unique, unmatched qualities when
dealing with remote locations, emergency situations, fluid conflict
zones, and as a final recourse against Internet shutdowns. However, they
are subject to their own specific risks which are impossible to fully
mitigate.

It should be presumed that sat phone conversations/messages are not
private without additional tools, and that usage of satellite
communications can be used to locate the device, particularly when
active for long periods of time. The requirements for an adversary to do
these are not significant, but do require some effort and will to do
so.

The commercial, end-user landscape of these tools is full of expensive
hardware, cost-prohibitive connectivity costs, legal and import/export
restrictions -- and a steep learning curve around the intentionally
obfuscated safety and security of the usage of the products.-->

<div class="notice--info">
<p><strong>A note on Alternative Communication Options</strong></p>
<p>While not in scope for this document, for situations such as preparation
for internet and/or electricity shutdowns, planning for multiple
alternative communication options adds resilience and enables more
flexibility during a crisis. Topics, plans, and tools can include:</p>
<ul><li>Planning for physical meetings (and contingency planning if there
   are safety concerns or limited movement options)</li>
<li><a href="https://en.wikipedia.org/wiki/Radio_frequency">HF/UHF/VHF Radio</a></li>
<li>Shortwave receivers to track international news</li>
</ul>
<!--***Note**: Contributions to supplement this guide with detailed
documentation on the operational and legal considerations of the above
would be welcomed.*
{: .notice--info}-->
</div>

# Summary of mitigations

[<i class="fas fa-download" aria-hidden="true"></i> DOCX](/assets/docs/satcom-mitigations-en.docx){: .btn .btn--info} [<i class="fas fa-download" aria-hidden="true"></i> PDF](/assets/docs/satcom-mitigations-en.pdf){: .btn .btn--info}

<table>
<tr>
<td><strong>Satellite communications are slow and expensive</strong></td>
<td><ul class="incremental">
<li>Avoid using the device for long periods of time.</li>
<li>For Internet Links, avoid activities that require a lot of speed or bandwidth.</li>
<li>Be mindful of the service’s billing.</li>
<li>Prefer to use more traditional technologies to make calls/connect to the internet if available.</li>
</ul></td>
</tr>
<tbody>
<tr class="odd">
<td><strong>Satellite communication devices can be geolocated</strong></td>
<td><ul class="incremental">
<li>Please only turn on satellite phones to make short calls, ideally from different places and away from home, work, etc.</li>
<li>Please only turn on the device for short periods of time. For a phone, only to make short calls. Keep in mind that some satellite devices take several minutes to set up and get connected.</li>
<li>Operate the device ideally from different places and away from home, work, etc.</li>
<li>Avoid multiple parties transmitting from the same location. Especially at different times.</li>
<li>For Internet links, locate the device as far from your exact location as possible, one strategy is to connect a wireless router to the link to receive Wi-Fi signal at a distance, or use cables and switches to gain space between the link and you.</li>
<li>Satellite devices with omnidirectional antennas are way easier to locate. Be careful.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Satellite communications might be intercepted and jammed</strong></td>
<td><ul class="incremental">
<li>Treat communication transmitted by satellite as untrusted and easily compromised, especially phone calls.</li>
<li>If possible, try to add extra layers of security, for instance, when using devices with internet data try to use applications and platforms that use encryption, like Signal or WhatsApp.</li>
<li>Be prepared for the connection to be affected, this can be done at the satellite level (more complicated), or at the local terrain level (easier)</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Be mindful of the physical environment</strong></td>
<td><ul class="incremental">
<li>Satellite devices use electricity as any other electronic equipment, prepare backup power solutions like power banks, solar chargers, generators, etc., and manage them efficiently.</li>
<li>The terrain also affects the reception quality, you will need to operate the device with a line of sight to the sky and avoid buildings, mountains, etc. that might block the signal.</li>
<li>Look for danger in the surroundings when operating the equipment. Avoid using it from a location that cannot be easily evacuated in case of an emergency or attack.</li>
<li>You can put camouflage (like cardboard, paper, cloth, etc.) on top of satellite antennas to conceal them and see if the service is good enough to operate without issues. Be mindful of the angle the antenna should point to the open sky, this will vary on the type of device.</li>
<li>Be mindful of your risks if carrying a satellite device with you at checkpoints, during raids, etc. One strategy might be storing the device in fixed locations, considering the advice above of not operating it from these places.</li>
<li>Using Bluetooth headsets might help you to gain some extra distance from satellite phones and raise less suspiciousness from carrying an unusual device.</li>
<li>Some devices cannot operate outside of specific temperatures, read the manual of your device to make sure that for instance, it won’t break below 0 Celsius. Make sure other devices, like routers, are always dry.</li>
</ul></td>
</tr>
</tbody>
</table>



# Detailed Risks and Mitigations

## Geolocation

**Multiple approaches can be used to geolocate an active satellite communications device regardless of the type of device**. While satellite phones are the easiest to track given their omnidirectional antenna, other devices such as BGANs and Starlinks are still locatable by multiple methods. These methods range from easy to use but expensive to low-cost DIY tools which are easy to source but require more skills. Military adversaries in a conflict zone are likely to be resourced with skills and devices and also likely to be actively scanning for satellite communications.

Geolocation methods include the following, see the Details section below for specific references and capabilities

* **Satellite-based tracking** - There are commercially available satellite-based offerings which enable fully global and remote location, tracking, and even custom alerts for "unexpected" satellite (and other radio frequency) signals. Intelligence satellites are an additional option for some countries.
* **Intercepting of GPS data** - Satellite devices often communicate GPS locaiton details which can be intercepted.
* **Radio Frequency (RF) monitoring and triangulation** - Geolocation tools can be mounted on aircraft and drones/UAVs for better detection of BGAN, Starlink, and other more directional connections, as well as locating signals where terrain or other obstacles limits ground-based tool effectiveness. RF monitoring tools (including simple, DIY ones) can also be mounted on vehicles or even be handheld. Tools can also be placed in fixed locations to track signals in an area over time.
* **Legal pathways** - In addition to technical means, there are also legal avenues (simply demanding records from satellite service providers directly and/or in the country(s) where their ground stations are located.

<!--
Satellite phones are the highest risk here due to their omni-directional
antenna setup.

As differentiated from devices which use large satellite
dish-style, directed antennas, Sat Phones are the easiest for an
adversary to geolocate due to their use of L band comms with an
omni-directional antenna. The band is a commonly monitored band, and the
omni-directional antenna means it has significant "spill-over" of RF
noise visible to direction finder devices. This risk is higher when the
phone is used or even left turned on for a long time. Even if not "used"
but only tuned on, the phone will send frequent pings to the satellite
which could be tracked for triangulation.

Any adversary capable of intercepting (see below) also has the potential
to receive precise GPS coordinates. These are in some cases transmitted
in the clear, and can be therefore discovered by capturing uplink and in
some cases much more widely available downlink signals as well.


-->

### Mitigations

**The longer a device is used, and the more times it is used from the same location over time, the more precise the location can be calculated and/or corroborated with other events or known locations** (such as office or house addresses, posting of news stories, social media engagement, etc.).

-   Minimize usage time - short calls or messages, very planned and prepared sending/receiving of data
-   If possible, use the device from a different location each time to reduce the ability for an adversary to correlate the device with a specific location over time.
-   Leave the device fully turned off when not in use
-   If the device also has cellular service (GSM/4G/etc.) disable that functionality when not in use to limit tracking by cellular tower triangulation.
-   Also practice the mitigations under device seizure, above.
    -   In specific, the use of a wireless router to give physical
        distance from the satellite device provides specific benefit
        here by giving you some warning of a raid or other targeted activity against the location
        of the device, as well as (in military/conflict situations) some
        distance from kinetic attacks such as missiles or other
        bombardment.
-  Where you use the device from impacts how easy it is to locate, track, and respond to by adversaries. There is no universal guidance here, and specific use cases, requirements, adversaries, and context play roles:
   - Consider the terrain / urban infrastructure and how it can help limit geolocation. In Afghanistan for instance, it's extremely difficult to use direction finding equipment due to the mountains and deep valleys, act as an automatic shield for signals.
   - Making sat-phone calls from highly populated areas can make it difficult
for law enforcement type authorities to identify and physically intercept the caller after a
short call. However, if facing military or state actors, this could instead add risk of bombardment of the area.
   - Using devices in locations far from urban areas, government
infrastructure, military installation/activity, and borders, and using
them for short periods of time and

### Details

#### Satellite-based tracking

"HawkEye 360 is a Radio Frequency (RF) data analytics company. We operate a first-of-its-kind commercial satellite constellation to identify, process, and geolocate a broad set of RF signals. We extract value from this unique data through proprietary algorithms, fusing it with other sources to create powerful analytical products that solve hard challenges for our global customers. Our products include maritime domain awareness and spectrum mapping and monitoring; our customers include a wide range of commercial, government and international entities."<br /> -- *HawkEye360 Press Release, (March 4 2022), [HawkEye 360 Signal Detection Reveals GPS Interference in Ukraine](https://www.he360.com/hawkeye-360-signal-detection-reveals-gps-interference-in-ukraine/) he360.com*
{: .notice}

{% include video id="hsxHk7kK-9U" provider="youtube" %}
*Video from HawkEye360 detailing commercial capabilities*

#### Radio Frequency (RF) Monitoring and Triangulation

"“Russia has spent a long time perfecting these techniques. On April 21, 1996, Chechnya’s breakaway president, Dzhokhar Dudayev, was speaking on a satellite phone with Russian envoy Konstantin Borovoi about setting peace talks with Yeltsin. **During the phone call, he was killed by a signal-guided missile fired from a Russian jet fighter. The warplane had received Dudayev’s coordinates from a Russian ELINT (electronic intelligence) plane that had picked up and locked on to the signal emitted by the satellite phone**. It was Russian deception and brutality at its finest."<br /> -- *Pelton, Robert Young (March 3 2012) [Kill The Messenger](https://foreignpolicy.com/2012/03/03/kill-the-messenger/), Foreign Policy.*
{: .notice}

"During our market scan, we found examples of SIGINT capabilities outside of government that are available to anyone. The capabilities we found have applications in maritime domain awareness; radio frequency (RF) spectrum mapping; **eavesdropping, jamming, and hijacking of satellite communications; and cyber surveillance**. **Most of these capabilities are commercially available, many are free, and some are illegal**. In our view, the existence of both legal and illegal markets and capabilities results in an environment where SIGINT has been democratized, or available to anyone. The capabilities we found have implications for the U.S." <br /> -- *Weinbaum, Cortney et al, (2017) [SIGINT for Anyone: The Growing Availability of Signals Intelligence in the Public Domain](https://www.rand.org/pubs/perspectives/PE273.html) RAND.*
{: .notice}

"**\[Satellite communications\] can be triangulated with affordable, even homemade tools.** […] Highly developed countries with advanced technical security are likely to have this capacity, less developed states and even non-state actors may be able to develop the capacity."<br /> -- *SMALL WORLD NEWS (March 2012) [GUIDE TO SAFELY USING SAT PHONES](https://gisf.ngo/wp-content/uploads/2020/02/2173-Small-Worls-News-2012-Guide-to-safely-using-satphones.pdf) The Global Interagency Security Forum.*
{: .notice}

"It is possible that the Syrian army used the long-established ‘direction-finding’ approach to pin-point the location of the journalists in the media centre. […] It is relatively simple to receive this signal for a trained technician, using an RF (Radio Frequency) spectrum analyser. […] After detecting the presence of sat phone transmissions, it would be relatively easy for communications technicians to find the location of the phone by tuning to that frequency, moving the antennas to find the direction where the signal was strongest and then triangulating with their opposites. This would provide an ever-shrinking triangle until the points intersect."<br /> -- *SaferMobile Anonymous Contributors (February 23 2012) [Be Afraid, Be Very Afraid of Satellite Phones in Insecure Locations](https://web.archive.org/web/20120327070537/https://safermobile.org/be-afraid-be-very-afraid-of-satellite-phones-in-insecure-locations/) SaferMobile.*
{: .notice}

#### Intercepting GPS Coordinates

"**It is very likely that the GPS location data is transmitted by the sat phone is sent in the clear**.  According to the specification (GSM-1 04.008 Section 10.1.8) the message from the sat phone requesting a channel carries among other information the dialed number and the GPS location data before the handset identity is established.  This makes the location data easily readable by an adversary."<br /> -- *SaferMobile Anonymous Contributors (February 23 2012) [Be Afraid, Be Very Afraid of Satellite Phones in Insecure Locations](https://web.archive.org/web/20120327070537/https://safermobile.org/be-afraid-be-very-afraid-of-satellite-phones-in-insecure-locations/) SaferMobile.*
{: .notice}

#### Legal pathways

"There are a few different ways by which satellite phones can be tracked.  The first—and easiest for a government actor—would be to simply ask or pressure a company to hand over user data."<br /> -- *York, Jillian and Timm, Trevor (February 2012) [Satphones, Syria, and Surveillance](https://www.eff.org/deeplinks/2012/02/satphones-syria-and-surveillance) EFF.*
{: .notice}

## Communication Interception

Similarly to the device geo-location options, interception of satellite communication has a range of technical options as well as legal pathways. Interception of satellite phone calls can take place nearby using ground-based equipment. Interception of any satellite device can take place by intercepting the signal from the satellite back down to its earthstation, or even by using commercial and private satellite options. Finally, a small number of nations have the ability to position satellites alongside (“co-orbital”) popular communication satellites to eavesdrop on communications to/from that satellite. While this is very rare and much more likely focused on military/defense outcomes, there are many similarly capable commercial options.

Further, research to date has revealed that the baseline security of the communication is not a priority for providers or the standards-setting bodies. **This means that without additional encryption, basic satellite communication is both insecure and easy to passively monitor.**

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

#### Baseline Encryption

"Modern satellite phones encrypt voice traffic to prevent eavesdropping. It's that modern GMR-2 algorithm that was the focus of the research, given that it's used in most satellite phones today. […] The end result was that **encrypted data could be cracked in a fraction of a second**. "This again demonstrates that there exists serious security flaws in the GMR-2 cipher, and it is crucial for service providers to upgrade the cryptographic modules of the system in order to provide confidential communication," said the researchers."<br /> -- *Whittaker, Zack  (July 6 2017) [New attack can now decrypt satellite phone calls in "real time"](https://www.zdnet.com/article/encryption-satellite-phones-unscramble-attack-research/) ZDNet.*
{: .notice}

"**[E]avesdropping on satellite communications is (in principle) easier than eavesdropping on cellular signals.** That’s because satellite ‘spot beams’ cover relatively broad geographic territories (Thuraya’s are 600km on average). So you don’t just have to worry about eavesdropping by your neighbor, you have to worry about eavesdropping by neighboring countries."<br /> -- *Green, Matthew  (February 5 2012) [Satellite phone encryption is terrible. Anyone surprised?](https://blog.cryptographyengineering.com/2012/02/05/sattelite-phone-encryption-is-terrible/) Cryptography Engineering.*
{: .notice}

#### Nearby (Tactical) Interception

"Proximity is relative. First you have to distinguish between what's commonly called "tactical" intercepts which are done in the field. For those, you receive the phone uplink but a phone transmits with quite a bit of power and doesn't have very directional antenna, so it can be several kilometers, especially if you have a good vantage point.  Then there is what's called "strategic" interception setups, done at dedicated facilities. What goes up must come down and most satellites are just "bent pipe", dumbly retransmitting what they receive back to earth. So instead of receiving the phone, you can just listen to the sat retransmitting the phone comms back to the ground station."<br /> -- *Sylvain  Munaut 2021 (paraphrased)*
{: .notice}

"The satellite doesn't do much," said Pavur. "It's basically just a dumb, bent pipe." It sends the data back to a base station on Earth, which then connects to the internet as usual. This part of the journey is very difficult for an attacker to intercept.  When data comes back from the internet, it heads to the satellite and back down to customers. This time, Pavur explains, the satellite blasts data across an enormous area in order to reach all of the satellite ISP's customers.
"This is the crux of satellite eavesdropping," he explained. Because the broadcast covers such a wide area, an attacker can easily intercept one side of the communications. … **Intercepting satellite communications can be done by someone in a different country, or even different continent, than the victim.**<br /> -- *-   Eddy, Max (August 6, 2020) [Sensitive Satellite Internet Data Is Easily Accessible, If You Know Where to Look](https://www.pcmag.com/news/sensitive-satellite-internet-data-is-easily-accessible) PCMag.*
{: .notice}


"One example of satellite eavesdropping was the use of the $26 Russian SkyGrabber program by hackers in Iraq to capture U.S. military Predator drone video feeds in 2009. **Insurgents eavesdropped on the unencrypted video feed backhauled from Predator drones through commercial communications satellites**. Surprisingly, such encryption weaknesses still exist for some commercial satellite systems. The government addresses this weakness by requiring encryption for military communications that rely on commercial systems, but other nongovernmental traffic through
those systems may remain vulnerable."<br /> -- *Weinbaum, Cortney et al, (2017) [SIGINT for Anyone: The Growing Availability of Signals Intelligence in the Public Domain](https://www.rand.org/pubs/perspectives/PE273.html) RAND.*
{: .notice}

“As the conflict grew, an increasing number of users migrated from Thuraya to other networks, both because of the interruptions associated with the intermittent jamming as well as a strong perception among many in the Libyan opposition that the Thuraya servers were especially vulnerable to LAJ signals intelligence or some other form of unspecified interception. […] It would become clear after the conflict ended that this concern was at least in part well-founded: the LAJ was found to have training materials for the L3 Communications Tactical Thuraya Monitoring System, an interception and localization package developed for field-deployed signals intelligence applications.”<br /> -- *Scott-Railton, John (January 2013) [Revolutionary Risks: Cyber Technology and Threats in the 2011 Libyan Revolution](https://digital-commons.usnwc.edu/cgi/viewcontent.cgi?referer=&httpsredir=1&article=1012&context=ciwag-case-studies) U.S. Naval War College Digital Commons / CIWAG Case Studies.*
{: .notice}

“By this point, the regime's electronic warfare had become even more sophisticated. Cell phone and landline calls had long been monitored, but now the spies turned their attention to satellite phones. To avoid NATO air strikes, one team of Ukrainian mercenaries set up shop in a kindergarten, right around the corner from the intelligence headquarters; **from there they snooped on sat-phone traffic using frequency scanners**. Gadhafi had declared that anyone caught with a satellite phone could be sentenced to death.”<br /> -- *Aikins, Matthieu (May 18 2012) [Jamming Tripoli](https://www.wired.com/2012/05/ff-libya/) Wired.*
{: .notice}

#### Global/Remote (Strategic) Interception

"The portfolio of Rohde & Schwarz satellite monitoring solutions for passive interception and monitoring of satellite communications signals is based on many years of professional experience. It ranges from flexible, transportable solutions to complex stationary strategic systems for simultaneous interception of signals and services from multiple satellites. Areas of application include the analysis and identification of unknown satellite based communications as well as the processing of satellite signals and services for intelligence purposes. Field-proven operational concepts and sophisticated analysis tools help organizations efficiently and effectively analyze carriers, services, content and metadata."<br /> -- *Rohde & Schwarz (Retrieved Mar 24 2022) [Satellite Intelligence](https://www.rohde-schwarz.com/us/products/aerospace-defense-security/satellite-monitoring/pg_overview_64135.html) rohde-schwarz.com [Archive](https://web.archive.org/web/20220324142831/https://www.rohde-schwarz.com/us/products/aerospace-defense-security/satellite-monitoring/pg_overview_64135.html)*
{: .notice}

"That new primary mission was “Thuraya collection and Afghanistan/Pakistan exfiltration.” The first confirms that the close placement near, and apparent co-orbital shadowing of, the commercial Thuraya 2 satellite is indeed intentional: Mentor 4 is indeed eavesdropping on Thuraya 2. The second relates to a more typical mission of ORION SIGINT satellites: collecting radio signals from a wide geographic region on Earth. The document also mentions (in the byline with the illustration) that the satellite was expected to be fully operational around mid-May of 2009. This tallies with the observed moment of Mentor 4’s arrival near 44 degrees east. It arrived there in late April of 2009, although it did not fully stabilize there until July 2009 (see diagram below.) Like PAN’s orbital behavior, the behaviour of Mentor 4 is unusual for a SIGINT satellite. The very close placement and closely synchronized co-orbital movement of Mentor 4 with regard to Thuraya 2 is unique, in the sense that it is behavior different from both earlier and later satellites in the ORION series: none of these shadow another satellite this closely." <br /> -- *Langbroek, Marco (Octover 31 2016) [A NEMESIS in the sky](https://www.thespacereview.com/article/3095/1) The Space Review.*
{: .notice}

"In a speech outlining France’s space policy and security issues, Parly said that the Athena-Fidus satellite, operated jointly by France and Italy, was approached “a bit too closely” by Russia’s Luch-Olymp craft, known for its advanced listening capacity. “It got so close that we might have imagined it was trying to intercept our communications,” she added. “Trying to listen to your neighbours is not only unfriendly, it’s an act of espionage.”<br /> -- *Chrisafis Angelique (September 7 2018) ['Act of espionage': France accuses Russia of trying to spy on satellite data](https://www.theguardian.com/world/2018/sep/07/france-accuses-russia-spying-satellite-communications-espionage) The Guardian*
{: .notice}

#### Groundstation Monitoring

"Governments can also intercept communications on satellite phones. **Satellite phone calls with a mobile phone or landline are routed through ground stations in numerous countries.** When transmitting through these ground stations, communications providers must comply with local legal and regulatory frameworks, making it possible for local governments to intercept private communications. " <br />--*OSAC Cybersecurity Team (July 2 2021) [Guide for Overseas Satellite Phone Usage](https://www.osac.gov/Content/Report/9db45731-1eec-477a-a7af-1bf950cb4013) OSAC.gov.* (**Also has a table of known laws**)
{: .notice}

<!--Last week’s news that China has installed a ground station for intercepting signals transmitted through the US and Russian communication satellite systems makes one wonder just how proof against interception and interruption are satellite communication systems. Unauthorized listening-in would seem to be unavoidable because the geostationary and near-geostationary satellites of the military and civilian systems radiate signals in all directions and these signals can be picked up by any ground station over nearly one-third of the Earth’s surface from which the satellite can be seen.<br /> --
 -- 1968 article https://www.newscientist.com/article/dn10536-china-can-eavesdrop-on-us-satellites/
{: .notice}
-->

## Legality and Seizure

Satellite communication tools, from phones to more robust data
connection setups, are often tightly regulated and may be illegal.
[OSAC's July 2021 report](https://www.osac.gov/Content/Report/9db45731-1eec-477a-a7af-1bf950cb4013)
has a list of countries where sat phones are known to be illegal.
Additional law tracking resources include [UNIDIR's Cyber Policy Portal](https://unidir.org/cpp/en), [GPD's Encryption Policy map](https://www.gp-digital.org/world-map-of-encryption/) , and [Cyrilla](https://cyrilla.org/).

In addition, due to the need for an outside, direct line of sight to the
sky - combined with visually distinct features from cell phones and
other equipment, satellite communication systems can be difficult to conceal.

Device seizure (and the further impacts that can have) is a very real risk to
consider. Device siezure can reveal your contact network, stored files, and
recent call logs, as well as be used potentially to impersonate you to
your contacts.

Further, given the illegality of non-registered devices in many
countries, possession/use alone can be enough to detain someone.

### Mitigations

-   Track which devices you are using (including smartphones and laptops) have what data stored on them.  Satellite phones and pagers are likely to have recent call logs and contacts. Regularly purge contacts, recent calls/message and any other content/documents on as many devices as possible - in particular ones which cannot be protected with encryption. Use automatically disappearing message options. Log out of apps/websites.
-   Use a bluetooth headset (for calls/satphones) or wifi connectivity / router to not be in possession of the device when you use it. (See device geolocation mitigations below)
-   If you are in a location where raids or similar physical searches are likely, find a safer location to store equipment, and carefully consider the potential value of the satellite device against the possibility of arrest. Should you dispose of or destroy this device instead?
-   If purchasing, seek out dual-use equipment, for example, devices which look like GPS units but which also provide a satellite data connection. If using this approach, ensure that users have a reason to use a GPS device and familiarity with its features.
- Consider your adversary -- are you trying to conceal your device from someone walking by on the street, or from someone flying over in a helicopter? Both?

**Additional guidance for satellite dishes and BGANs**

- **Concealment** -- limit how visible the device is when it is outside:
  - BGANs are directional (as opposed to omnidirectional satellite phones) and require specific angles of visiblity to the sky. [This map](https://www.groundcontrol.com/products/inmarsat/bgan-range/bgan-coverage-map/) provides a very rough idea of the angles (both compass directional and vertical) that you will need for BGANs depending on your location.
  - Starlink terminals require a 100° cone up from the dish, which will calibrate itself to the ideal base angle depending on your location.
  - Understanding what angle your device requires allows you to minimize its visibility from other directions - including to some extent from above in the case of BGAN and other directional dishes pointing at geostationary satellites.
- **Camoflauge** -- different materials will have different effects if covering a satellite dish. In general, any covering is likely to reduce your signal. Consider lightweight, dry cloth or plastic, or non-metallic paint.
- As you explore your concealment options, review your device's diagnostics tools to see how that is impacting its connectivity.

### Details

A week after shutting down the internet for the second time in two months, the Senegalese government is arresting people selling Starlink in the country for “illegal provision of internet access and irregular marketing”. <br /> On Monday, the Senegalese government arrested five people for selling Starlink terminals without the required licence or authorisation. The five people arrested by the Department of Urban Security of the National Police face up to five years imprisonment and a fine of 60 million CFA ($100,000). The telecommunications regulatory authority has also issued a warning for any service providers marketing Starlink and any other company with similar activities to immediately cease all service throughout the country." <br /> -- *Oladunmade, Muktar (Aug 08, 2023) [Starlink sellers arrested in Senegal](https://techcabal.com/2023/08/08/starlink-senegal/) TechCabal.*
{: .notice}

"OSAC members have reported difficulties importing satellite phones in countries where the devices are technically permitted (or not restricted). In Libya, there are no laws against satellite phones, but there have been multiple reports of authorities confiscating satellite phones, GPS devices, and personal tracking devices at the airport. "<br />--*OSAC Cybersecurity Team (July 2 2021) [Guide for Overseas Satellite Phone Usage](https://www.osac.gov/Content/Report/9db45731-1eec-477a-a7af-1bf950cb4013) OSAC.gov.* (**Also has a table of known laws**)
{: .notice}

## Jamming

Jamming is used to block all communications in an area (downlink) or
with a specific satellite (uplink). Both are relatively easy and
inexpensive, but untargeted. Jamming a satellite (uplink) can have
international impacts and would be a breach of ITU's [Article
15](https://www.itu.int/en/ITU-R/terrestrial/tpr/Documents/Article15-RR16.pdf),
Interference from Radio Stations, and will be quickly noticed internationally.  GPS signals can also be targeted for jamming, which inhibits satellite devices from connecting and staying connected with satellites.

Jamming may not be targeted at you specifically, but could still impact your ability to connect using satellite communications -- you may be a bystander to jamming targeted in the area and/or against the same satellites you are using.

Finally, environmental factors may also cause failed connectivity. Weather and/or other obstructions between your satellite device and the sky (dependent on the type of device, it's precise angle to aim at the satellite, etc.) all can cause connectivity issues.

### Mitigations

-   Downlink jamming in range dependent and must be within line of sight,
    moving to a different area could get outside of the area of effect.
    *Consider if your adversary is trying to force you to move.*
-   Uplink jamming is often scheduled around specific events or times of day, try testing connectivity at different times.

### Details

"There are two main types of satellite jamming. The first, uplink jamming, interferes with the signal going from a ground station or user terminal to the satellite. An RF signal of the same frequency as the targeted uplink signal is transmitted to the satellite, aiming to limit the satellite transponder from differentiating between the jamming signal and the actual signal. The second type, downlink jamming, disrupts transmissions sent from the satellite to ground-based or airborne receivers using RF signals that mimic the frequency of the downlink signal. It aims to inhibit ground users from receiving transmissions from the satellite and only needs to be as strong as the signal being received on the ground. Uplink jamming is considered more difficult because greater transmitter power is required to reach a given satellite’s transponders. It could be more impactful, however, due to its ability to degrade the satellite’s signal for all its users. Because downlink jammers must be within the field of view of the receiving terminal’s antenna, however, the effects of downlink jamming are more localized."<br /> -- *Velkovsky, Pavel; Mohan, Janani; and Simon, Maxwell (April 03 2021) [Satellite Jamming](https://ontheradar.csis.org/issue-briefs/satellite-jamming/) On the radar / CSIS.*
{: .notice}

"Jamming technology tends to be commercially available and relatively inexpensive. **Satellite jamming systems are easy for states and non-state actors to develop given the relative low cost of their procurement and operation.** There is a low threshold of technological competency required to perform jamming, and the technology is available to a plethora of actors across the globe. For example, interference with satellite signals has emanated from Indonesia, Cuba, Ethiopia, Libya, and Syria, among others."<br /> -- *Velkovsky, Pavel; Mohan, Janani; and Simon, Maxwell (April 03 2021) [Satellite Jamming](https://ontheradar.csis.org/issue-briefs/satellite-jamming/) On the radar / CSIS.*
{: .notice}


#### Downlink / Ground-based / Terrestrial Jamming

“It is true that the Starlink ground terminals will be broadcasting, and thus potentially targetable using RF signal detection equipment. But I doubt they’d be that high of a priority for Russian targeting, so I think the odds of them being targeted is probably low,” Weeden said Monday by email. “A much bigger challenge would be Russian ground-based mobile jamming, which is sophisticated and can already deal with existing satellite signals such as GPS and satellite communications.”<br /> -- *Berger, Brian (February 28 2022) [SpaceX heeds Ukraine’s Starlink SOS](https://spacenews.com/spacex-heeds-ukraines-starlink-sos/) SpaceNews.*
{: .notice}

"Terrestrial jamming takes place in a specific location and involves equipment that is easy to purchase, use and conceal. Rather than targeting the satellite itself, as is the case in orbital jamming, terrestrial jamming involves transmitting rogue frequencies in the direction of local consumer-level satellite dishes. The contradictory frequencies are area-specific, interfering only with the frequency emanating from the satellite in a specific location. **Small, portable terrestrial jammers have a range of 3-5 kilometres in urban, built-up areas. In rural areas, their range can increase to up to 20 kilometres**"<br /> --  *Small Media (November 2012) [Satellite Jamming in Iran: A War Over Airwaves](https://smallmedia.org.uk/work/satellite-jamming-in-iran-a-war-over-airwaves), Small Media.*
{: .notice}

"When HawkEye 360 analysts examined Ukraine over the past four months, they discovered continued and increased GPS interference across the region. The data showed extensive GPS interference in November 2021 along the boundary of the pro-Russian separatist-controlled regions in Luhansk and Donetsk. Open-source information confirmed Unmanned Aerial Vehicles (UAVs) operating in the area were disrupted due to lost GPS connections… And in February 2022, HawkEye 360 detected GPS interference along the border between Ukraine and Belarus, shortly before the Russian invasion started." <br /> --*HawkEye360 Press Release, (March 4 2022), [HawkEye 360 Signal Detection Reveals GPS Interference in Ukraine](https://www.he360.com/hawkeye-360-signal-detection-reveals-gps-interference-in-ukraine/) he360.com*
{: .notice}

"The jamming of Persian-language satellite channels has been ongoing since 2003. Infrequent bouts of pressure from the international community have achieved limited success. Alongside international organisations like the International Union (ITU), the governments of the UK, US, France and the European Union have condemned the Iranian government for not acting on the issue of satellite jamming. **Despite these condemnations, the jamming of satellite TV channels has continued.** At the time of publishing, the sudden devaluation of the Iranian Rial in October 2012 had spurred another intense period of jamming, with the broadcasts of both BBC and the VOA being disrupted … **It is important to note here that Iran is not the only country engaged in or experiencing satellite jamming. There are reports of jamming from countries such as Bahrain, Libya, Syria, Ethiopia, North Korea, and China.**"<br /> --  *Small Media (November 2012) [Satellite Jamming in Iran: A War Over Airwaves](https://smallmedia.org.uk/work/satellite-jamming-in-iran-a-war-over-airwaves), Small Media.*
{: .notice}

#### Uplink / Satellite Jamming

“Over the weekend of February 19, transmissions from two television satellites that served a wide range of news programming to Libya and the region were disrupted by jamming, according to the Lebanese Telecommunications Regulatory Authority. And on February 21, Al Jazeera accused Libya of jamming its satellite transmissions in the region, and stated that it had conclusively identified the jamming as emanating from an LAJ intelligence services building south of Tripoli. <br />Satellite telecommunications were not immune to LAJ disruption and denial efforts, which were likely targeted against the use of satellite telephones like the Thuraya handset, which were widely used in Libya. On February 25, Thuraya accused Libya of having engaged in a week’s worth of jamming of the Thuraya-2 satellite that provided satellite phone and data connectivity to Thuraya devices within Libya. Shortly thereafter, Thuraya announced that its technical efforts had restored voice services to much of Libya. Nevertheless, users of Thuraya phones continued to experience substantial difficulty connecting throughout the revolution.”<br /> -- *Scott-Railton, John (January 2013) [Revolutionary Risks: Cyber Technology and Threats in the 2011 Libyan Revolution](https://digital-commons.usnwc.edu/cgi/viewcontent.cgi?referer=&httpsredir=1&article=1012&context=ciwag-case-studies) U.S. Naval War College Digital Commons / CIWAG Case Studies.*
{: .notice}

"Jamming can also occur accidentally: in 2015, U.S. military officials noted they were unintentionally jamming satellite communications an average of 23 times per month. Purposeful jamming can be difficult to differentiate from accidental interference, making attribution more challenging."<br /> -- *Velkovsky, Pavel; Mohan, Janani; and Simon, Maxwell (April 03 2021) [Satellite Jamming](https://ontheradar.csis.org/issue-briefs/satellite-jamming/) On the radar / CSIS.*
{: .notice}

## Satellite Systems Security

Both the user-facing devices (phones, terminals, modems) and the space-based satellites and their groundstation infrastructure also face classic cybersecurity risks of compromise, DDoS, and similar vulnerabilities rendering them unsafe or unusable.

### Mitigations

-   To the extent possible, leverage satellite communications devices as untrusted network connections and layer on independent security.
-   Consider having a further backup communications plan if satellite connectivity stops working. This could include alternative satellite connectivity options using different providers.
-   Check the manufacturer website for your device to ensure you have the latest possible firmware.
-   If you operate a network using satellite uplinks, see also this checklist from US's CISA (Cybersecurity and Infrastructure Security Agency) [Strengthening Cybersecurity of SATCOM Network Providers and Customers ](https://www.cisa.gov/news-events/cybersecurity-advisories/aa22-076a)

### Details

#### Attacks against Satellite infrastructure

"The situation in Ukraine has demonstrated dependencies on space-based technologies (Starlink, for example, and other satellites and communications networks) during conflict. In 2024, we expect to see evidence of sophisticated state-sponsored cyber actors’ full spectrum Computer Network Exploitation capabilities to compromise space-based and associated ground support infrastructure and communications channels to interdict, disrupt, deny, degrade, destroy, or deceive an adversary—as well as to conduct espionage" <br /> *- Carmakal, Charles; Joyce, Sandra; Potti, Sunil; Venables, Phil; et al. (November 8, 2023) [Cybersecurity Forecast 2024](https://services.google.com/fh/files/misc/google-cloud-cybersecurity-forecast-2024.pdf") Google.*
{: .notice}


"However, the attack against Viasat may not have involved jamming. The attack against the network was a “deliberate, isolated, and external cyber event,” according to Viasat spokesperson Chris Phillips. The attack only impacted fixed broadband customers and didn’t cause disruption to airlines or Viasat’s US government clients, the company says, and no customer data was impacted. However, people’s modems have not been able to connect to the network, and they have been “rendered unusable.”" <br /> -- *Burgess, Matt (March 23, 2022) [A Mysterious Satellite Hack Has Victims Far Beyond Ukraine](https://www.wired.com/story/viasat-internet-hack-ukraine-russia/) Wired.*
{: .notice}

"According to Colaluca, on February 23, at around 5 p.m. local time, before the modems were disabled, someone attempted to log into a Viasat appliance using several sets of valid credentials, although those attempts failed. An hour later, "there was a successful unauthorized access through that VPN, which landed in the core node, but nothing happened," at least initially, Colaluca said. About two hours after that, the attackers accessed the management server that was in place inside the core node with a different set of credentials. <br /> "From that point, over the next three to four hours, the attackers did a couple of things," Colaluca said. "One, they went to a network operations server that was present there, and its primary purpose was modem diagnostics, modem health, and how many modems are online. So that server had access to all the modems in the network in those two partitions, and they did recon work." <br /> The attack appeared targeted, with the attackers seeking particular sets of modems in certain regions for specific customers and specific functions, learning how many modems were online. An hour later, at about midnight, the attackers accessed Viasat’s FTP server, a part of the infrastructure that delivers new software or updates to the modems. They dropped a wiper binary along with scripts to enumerate the network, interrogate it, and report back the status after the scripts completed execution." <br /> -- *Brumfield, Cynthia (Aug 16 2023) [Incident response lessons learned from the Russian attack on Viasat](https://www.csoonline.com/article/649714/incident-response-lessons-learned-from-the-russian-attack-on-viasat.html) CSO Online.*
{: .notice}

"In a presentation at the Black Hat security conference in Las Vegas, Johannes Willbold, a PhD student at Germany's Ruhr University Bochum, explained he had been investigating the security of satellites. He studied three types of orbital machinery and found that many were utterly defenseless against remote takeover because they lack the most basic security systems. "People think that satellites are secure," he said. "Those are expensive assets and they should have encryption and authentication. I assume that criminals think the same and they are too hard to target and you need to be some kind of cryptography genius. Maybe it wasn't a good idea to give this talk." " <br /> -- *Thomson, Iain (Aug 11 2023) [Want to pwn a satellite? Turns out it's surprisingly easy](https://www.theregister.com/2023/08/11/satellite_hacking_black_hat/) The Register.*
{: .notice}

"The agencies have advised SATCOM network providers and customers to **use secure authentication methods**, enforce a **principle of least privilege**, review existing trust relationships with IT service providers, **implement independent encryption, strengthen software and firmware security, monitor their networks for suspicious activity, and ensure that they have incident response and resilience plans in place**." <br /> -- *-  Kovacs, Eduard (March 18 2022)[SATCOM Cybersecurity Alert Issued as Authorities Probe Possible Russian Attack](https://www.securityweek.com/satcom-cybersecurity-alert-issued-authorities-probe-possible-russian-attack) Security Week.*
{: .notice}

#### Attacks against end-user devices

"\[S\]atellite modems belonging to tens of thousands of customers in Europe were knocked offline. … The hackers disabled modems that communicate with Viasat Inc's KA-SAT satellite, which supplies internet access to some customers in Europe, including Ukraine. More than two weeks later some remain offline, resellers told Reuters. … The Viasat official said a misconfiguration in the "management section" of the satellite network had allowed the hackers remote access into the modems… He said most of the affected devices would need to be reprogrammed either by a technician on site or at a repair depot and that some would have to be swapped out.<br /> --  *Pearson, James, et al (March 11 2022) [Exclusive: U.S. spy agency probes sabotage of satellite internet during Russian invasion, sources say](https://www.reuters.com/world/europe/exclusive-us-spy-agency-probes-sabotage-satellite-internet-during-russian-2022-03-11/) Reuters.*
{: .notice}

"Between October and December last year, researchers from IOActive analyzed the firmware of popular satellite communications (SATCOM) devices that are used in the military, aerospace, maritime, critical infrastructure and other sectors… The analysis focused on SATCOM terminals that are used on ground, in the air and at sea, not satellite communications equipment in space. "IOActive found that **all devices within the scope of this research could be abused by a malicious actor**," the IOActive researchers said in a report published Thursday. "We uncovered what would appear to be **multiple backdoors, hardcoded credentials, undocumented and/or insecure protocols, and weak encryption algorithms**."<br /> -- *Constantin, Lucian (April 18 2014) [Satellite communication systems rife with security flaws, vulnerable to remote hacks](https://www.computerworld.com/article/2698346/satellite-communication-systems-rife-with-security-flaws--vulnerable-to-remote-hacks.html) ComputerWorld.*
{: .notice}

"Unfortunately, except for Iridium, the vendors did not engage in addressing this situation," the researchers said. "They did not respond to a series of requests sent by the CERT Coordination Center and/or its partners."<br /> -- *Santamarta, Ruben  (2014) [A Wake-up Call for SATCOM Security](https://ioactive.com/pdfs/IOActive_SATCOM_Security_WhitePaper.pdf) IOActive.*
{: .notice}


# Commonly overlooked challenges

Most of this document focuses on the operational security challenges and
mitigations involved in using satellite communications. However, there
are some baseline requirements to also keep in mind to simply ensure the
service is available when and if you choose to use it.

## Electricity

All satellite communications devices require power. VSAT and Starlink Dishes require anywhere up to 100
watts while actively transmitting, which can rapidly exhaust a battery
backup / UPS system. Satphones, pagers, and BGANs come with batteries capable of up
to 3 hours active time and 30 hours idle.

### Mitigations

-   Make sure your satphone/pager/BGAN is fully charged, re-charging when power is available.
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
-   Top up / add funds to / pre-purchase bandwidth for your satellite devices (this may be topping up your SIM card for a satphone/pager or BGAN) ahead of time.
-   Do not use satellite communications when other options are available.
-   Strictly plan and limit your usage time.
-   Know how your plan works if you reach your usage limit: will it stop
    working until you manually add funds? Will it continue at lower
    rates? Will it continue and charge overage fees?
-   Have a person outside of the conflict who has the information needed
    to track usage and provide additional account funds / recharge the SIM if the conflict is extended, or
    if you are unable to continue funding it directly (this could be due
    to other issues such as banking problems, or
    over-compliance/confusion around sanctions). This can protect
    against loss of access leading to an inability to regain access.

## Coverage and connectivity

When selecting devices, ensure that they have coverage in the areas they will be (or could potentially be) used. This is relevant both at a country level as well as a more specific daily usage level.  Satphones will not likely work inside, and will need to be outside to get a connection. IN addition, not all services work in all locations. This [at phone reseller provides a [good collection of coverage maps](https://www.satphonestore.com/coveragemaps), but check before purchase.

## Preparation

Voice calls via satphone can have bad audio, background noises, signficant delays/latency and overall poor call quality. Particularly if calls will be happen (possibly in emergency situations) between people communicating who aren't native speakers of the same language, preparation and training on how to communicate effectively in these situations is critical.

### Mitigations

*  Much like with communicating via radio, it is handy to have staff briefed before on things like the [NATO alphabet](https://en.wikipedia.org/wiki/NATO_phonetic_alphabet) or other simple, pre-arranged codewords.
*  Use 2-way good radio etiquette to help with latency problems, see this [Two-Way Radio Protocol by California State University](https://www.csudh.edu/Assets/csudh-sites/dhpd/emergency-preparedness/two%20way%20radio%20protocol.pdf).

# Glossary of terms

-   **"Bent Pipe"** - a term used to discuss "how" satellites deal with communication -- for the most part, the satellite simply relays the signals it receives directly between the device and the groundstation.
-   **BGAN** - Broadband Global Area Network - Inmarsat's portable satellite internet and related hardware
-   **Direction-Finding** or DF equipment - are tools which can help track the location of satellite (and other!) communication equipment. These systems can be permanently mounted, or used as hendheld kits or placed on vehicles or aircraft/drones.
-   **Downlink** - the broadcast from the satellite in orbit back down. Generally the "footprint" of these cover wide areas (hundreds of miles) each.
-   **ELINT** - A subset of SIGINT ("SIGnals INTelligence"), [ELINT ("ELectronic INTelligence")](https://en.wikipedia.org/wiki/Signals_intelligence#ELINT_and_ESM) focuses on only the radio frequency and related electronic components of communication, to support geolocation, signal jamming, and interception needs. A common term in researching satellite communication security.
-   **GEO** - [Geostationary orbit](https://en.wikipedia.org/wiki/Geostationary_orbit) ("Geosynchronous Earth Orbit") - a satellite, often for communications, which is in an orbit such that it is always in the same location in the sky above a fixed point on the Earth's equator. These are high orbits, so there is additional latency in communications.
-   **Groundstation** Also referred to as a "teleport", Earth Stations, and [Satellite Earth Stations ("SES")](https://en.wikipedia.org/wiki/Ground_station)) - Satellites relay the comms to dedicated ground stations where the data/call rejoins the "normal" terrestrial internet. Groundstations are strategically located for satellite visibility, but may be in countries without strong human rights or data privacy track records. ***Ground Stations can also refer to any two-way satellite communications terminal on the ground.***
-   **LEO** - [Low Earth Orbit](https://en.wikipedia.org/wiki/Low_Earth_orbit) - Due to their lower orbit, satellites in LEO offer higher bandwidth and lower latency, but require more satellites to cover a communication area.  Iridium and Starlink are examples of LEO communications satellite systems.
-   **Radio Frequency (RF)** - for the purspose of this guide, the [signals](https://www.techtarget.com/searchnetworking/definition/radio-frequency) used by satellite communication devices - but also cell phones, radios, and TV -- which can be blocked, intercepted and detected remotely. Specific frequencies are [reserved](https://en.wikipedia.org/wiki/Frequency_allocation) for specific applications, internationally by the ITU and per-country by regulation.
-   **Satphone** / **handset** - a device in the form factor of a large cell phone with a non-directional antenna.
-   **Uplink** - the communication from the satellite device up to the satellite in orbit. Directional antennas (dishes) limit the area one must be to intercept this, but most sat phones do not have directional antennas.
-   **VSAT** - "[Very-small-aperture terminal](https://en.wikipedia.org/wiki/Very-small-aperture_terminal)" - a two-way groundstation with a dish antenna smaller than 3.8 meters (so most satellite internet antenna like for starlink). These tend to require some "aiming" to make a connection.
{: .notice}
