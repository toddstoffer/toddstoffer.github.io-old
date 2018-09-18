---
layout: slide
title: Achieving Essential Digital Preservation
excerpt: "A lightning talk at the 2018 Code4Lib Southeast conference focused on the creation and deployment of a digital preservation platform at NCSU Libraries"
theme: simple
transition: convex
tags: [presentation]
category: presentation
---
<section data-markdown data-separator-notes="^Note:">

## Achieving Essential Digital Preservation
#### July 28, 2018 | Atlanta, GA

[Todd Stoffer - NCSU Libraries](mailto:tdstoffe@ncsu.edu)

[@toddstoffer](www.twitter.com/toddstoffer) | [tdstoffe@ncsu.edu](mailto:tdstoffe@ncsu.edu) | [go.ncsu.edu/c4lse](https://go.ncsu.edu/c4lse)

Note: Hello, I'm Todd and I am from NCSU. Today I am here to talk about digital preservation and the development of a new digital preservation application at NCSU Libraries. Here is some contact info and a link to the slides with speaker notes.
</section>

<section data-markdown data-separator-notes="^Note:">
## ~~Essential~~ Digital ~~Preservation~~

Note: Lets start by adding some context to the term digital. All libraries have digital assets. Ours, like most, come from a variety of sources (some digitized, some born digital, in a variety of formats (text, image, video) and all with a variety of differing preservation needs. Even though they are digital the issues related to scarcity and monetary value that are often used to determine preservation requirements of physical objects are still relevant. Due to the growth of these types of assets within our collections at NCSU, the need for a formal technical system to manage their longterm preservation, outside of our normal IT backup infrastructure, became a pressing matter.
</section>

<section data-markdown data-separator-notes="^Note:">

## ~~Essential~~ ~~Digital~~ Preservation

Note: To formally address our digital preservation needs NCSU Libraries established a working group (the Digitization and Digital Curation Working Group (DDCWG)). This group worked to identify our current digital preservation strategy and compare that to current best practices (many of which are outlined by the National Digital Stewardship Alliance (NDSA) “Levels of Digital Preservation" document) [1]. This resulted in a report outlining steps we could take to improve our current strategy and bring it more in line with industry best practices. By breaking this work down into levels of preservation it allowed us to begin thinking of technical solutions that could help us incrementally improve - level up. This is an important step in helping to avoid the preservation rabbit hole.

[1]https://www.digitalpreservation.gov:8081/ndsa/activities/levels.html
</section>

<section data-markdown data-separator-notes="^Note:">
## Preservation Rabbit Hole

Note: Often when we begin new digital preservation projects, we begin with good intentions of simply trying to keep some files around so we can use them again a few years down the road. However, soon enough we are down the rabbit hole of trying to develop a process that covers every 'what if' scenario. While I don't want to diminish the effect that a zombie apocalypse would have on our ability to maintain long-term preservation of word perfect files - a much more likely scenario is a simple drive failure and missed backup that could lead to the loss of digitized assets which would require a high cost to re-digitize and recover. By trying to remediate all potential negative outcomes, we are overcome with possibilities and delay the implementation of any technical solution at all.
</section>


<section data-markdown data-separator-notes="^Note:">

## Essential ~~Digital~~ ~~Preservation~~

Note: Are there certain aspects of digital preservation that are more 'essential' than others? This is the basic question that we started with. At a bare minimum what do we need to have in place before we feel that an asset is preserved. What concrete steps can we take to move up to higher levels as outlined by the NDSA which will improve our overall strategy. By working towards developing a solution that begins by addressing the low-hanging-fruit of digital preservation we have been able to avoid the rabbit hole that plagues so many digital preservation projects.
</section>

<section data-markdown data-separator-notes="^Note:">
## Introducing SCPS
### (noun | **\ˈsküps \\**)

Note: SCPS is an application developed by a team at NCSU Libraries that is focused on providing the basic DAMS functions of file tracking, checksum polling and notification of corrupt assets. It is a Ruby on Rails application that has been developed to be intentionally simple - while at the same time meeting the basic functional requirements of a digital preservation system. It was developed in collaboration with the Digital Library Initiatives department and the Special Collections Research Center.
</section>

<section data-markdown data-separator-notes="^Note:">
## SCPS Team
#### Bret Davidson

##### Brian Dietz

##### Todd Stoffer

##### Trevor Thornton

Note:
</section>

<section data-markdown data-separator-notes="^Note:">
## What Does it Do?

- Asset Ingest and Transfer
- Checksum Validation
- Failure Notifications

Note: At its most basic, SCPS just moves files into preservation storage. It takes files from local file systems or other servers and copies them to preservation storage mounts. It also records the destination locations of each asset, records a checksum of the asset and a bit of additional metadata. It also does regularly scheduled checksum comparison and sends notifications if there are discrepancies.
</section>

<section data-markdown data-separator-notes="^Note:">
![slide-image](/images/c4lse/basic-scps.png)

Note: So this is the basic implementation of SCPS. There is a staging storage mount and files that are to be ingested get put there - then they are run through SCPS, copied to additional preservation mounts and a variety of db records are created. Perhaps a better term than basic for this initial implementation would be foundational. This application is meant to serve as the foundation for our digital preservation process - and can and will be integrated into other systems to create a more complex soution.
</section>

<section data-markdown data-separator-notes="^Note:">
![slide-image](/images/c4lse/etd-integration.png)

Note: What does a SCPS integration look like? With only a slight amount of integration work we are able to preserve the output of other systems. Lets take a look at a recent enhancement we have been working on - using SCPS as an additional preservation location for our Electronic Thesis and Dissertations service. In this case we simply share a staging mount between two systems and can run a process to ingest a copy of each file in the secondary system.
</section>

<section data-markdown data-separator-notes="^Note:">
![slide-image](/images/c4lse/aptrust.png)

Note: And to extend it one more time - we can add 3rd party preservation endpoints to the storage array - giving us the ability to easily transfer data to off site storage providers.
</section>

<section data-markdown data-separator-notes="^Note:">
## Future Enhancements
- Additional 3rd Party Preservation Locations
- File Browsing / Access
- API Integration for Internal Systems
</section>

<section data-markdown data-separator-notes="^Note:">

## Thanks To:

##### Bret Davidson

##### Brian Dietz

##### Trevor Thornton
</section>

<section data-markdown data-separator-notes="^Note:">

## Thank You
#### @toddstoffer | tdstoffe@ncsu.edu

</section>
