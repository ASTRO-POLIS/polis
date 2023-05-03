# POLIS - Public Observatory Location and Information Service

**POLIS** is a new open standard that provides a hierarchical directory of distributed services that lists astronomical observing sites across the world and allows them to interact with each other and to the wider community of professional and amateur astronomers alike.

The standard offers three increasing levels of service functionality:

1. A pseudo-static information service that describes observatory facilities, instruments, devices, and configurations. It is updated on demand, either manually or automatically when there are changes at a facility.
2. A long-term observation request and reservation system.
3. A real-time observation scheduling and observatory monitoring system that facilitates observatory-to-observatory communication and collaborative observations.

## What is POLIS Service Provider?

A POLIS Service Provider (PSP) is a web service that lists observing sites and strictly complies to the POLIS Standard (formats) and query APIs. To be a valid PSP, the site need only implement the first level of POLIS services, which makes it a "Level 1 PSP". Implementation of the second and third level of services is optional. 

There are 5 types of providers:

- `Public` sites conform strictly to the POLIS standard, and provide APIs in the JSON format at a minimum. The site *must* list all known observatories (Earth-based and otherwise).
- `Private` sites are used locally by different organisations to support internal infrastructure or as a performance cache.
- `Local` sites can be used for clients running on mobile devices or desktop apps. They are used as a local cache and, in the case of mobile apps, in offline mode.
- `Mirror` sites are backups of public sites. These should only be used when the public site is down, either for maintenance or because of technical issues.
- `Experimental` sites are used for implementing and testing new functionality or future unstable versions of the POLIS standard.

## Goals

1. Provide a comprehensive and up-to-date directory of every observatory in the solar system for use by researchers, students, developers, and the public.
2. Creating a way for observatories to receive and handle observation proposals that is both easy for them and equitable for those seeking to use their facilities.
3. Enable professional and amateur observatories alike to coordinate observations and collaborate in the pursuit of a shared goal.
4. Empower amateur astronomers by exposing them to educational organisations and institutions in their area.

- can list any type of facility: ground based, satellite, mobile, temporary (e.g. solar eclipse),...
- can be used as datasource for mobile apps as well as for various web UIs and JSON/XML based APIs.
- supports API versions and of JSON and XML formats (XML is preferred for production sites; supporting additional formats is also permitted)
- observatories can provide data either manually or with standard APIs

A fully-implemented Level 3 POLIS Service Provider enables its observatory to utilise its available observation time in the most efficient way possible. Many observatories lie dormant on clear nights simply because no one has requested observation time. By connecting the observatory to the POLIS ecosystem, one can expose it to more people searching for a place to carry out their observations.

By providing a centralised place for astronomers to make their observing proposals, they can be exposed to scientific instruments that fit their needs but that they were previously unaware of. This can help alleviate bottlenecks at high-traffic observatories and reduce average wait times for observers.

POLIS is an important tool for the astronomy community, providing a way to connect observatories and researchers around the world and enabling collaborative research and scientific discovery.


## Further Documentations
**Note:** the most current version of the documentation, sketches for new ideas, and different example files can be found in the `dev` branch.
- ...

## How To Contribute

We are currently building a list of all known (to us) observing sites, and we will be making it publicly available soon. This information is inherently limited by the fact that almost none of it is first-hand—it's merely scraped from the internet. The best people to keep this information correct and up-to-date are, of course, the people who run the observatories themselves. **Please contact us** if you are interested in maintaining this information, either for your own institution/observatory or for one you are familiar with. We will be happy to provide beta versions of tools to perform this task easily. When stable, these tools will also be made public domain.

We are currently working on a macOS app to manage a POLIS Service Provider site. The app is in a very early stage (we still do most of the editing with a text editor), but if you are interested in managing a PSP site and use a current version of macOS, drop us an email at polis-support@tuparev.com.
- If you are an amateur astronomer, we'd be delighted to talk to you! One of our goals is to create a standard that is open and useful to everyone. Drop us an email at polis@tuparev.com with any comments, questions, or suggestions. 

## History
The initial idea for a POLIS like protocol was first discussed at one of the HTN (Heterogeneous Network of Telescopes) conferences that took place about a decade ago in Tucson (AZ) and Göttingen (Germany). Initially an agent-based system that negotiates the exchange of observation time was discussed. The idea was to use RTML's `Dump` mode to describe the current status and capabilities of an observatory and to build a new negotiation protocol.

Around 2012, the [StarCluster](www.starcluster.app) team developed a very primitive prototype that was able to exchange status information between two imaginary observatories, but further development did not take place.

The idea for such a protocol was reborn in early 2019 when the StarCluster team started working on a new package of astronomy applications. In September 2020, [ASA](https://www.astrosysteme.com) and StarCluster worked together on a joined  bid for a new robotic telescope and it was during this period when the decision was made to start a new open source project with the goal to create a protocol and database of modern observatories, which monitor and report their status, and to allow individual sites to negotiate automatically or with human support for observation times and joined observation schedules.

Rick Hessman, University of Göttingen (Germany) coined the name POLIS and introduced the StarCluster team to the work of Rachel Street, who independently developed a database for monitoring observatory statuses.

In November 2020 the ASTRO-Polis project was created on GitHub.
