# POLIS - Public Observatory Location and Information Service


## What is POLIS?
As the name suggests, the Public Observatory Location and Information Service provides a directory type of distributed services (similar to DNS) listing astronomical observing sites across the world as well as satellites. Three levels of services are offered:

1. The Observatory Location and Information service describes the Observatory Facilities. It is only updated on demand (automatically, or manually) when there are changes at the facility.
2. Currently known status changes and long-term night by night scheduling and observation reservation system.
3. Real time status changes and observation scheduling, facilitates  for observatory to observatory real time communication and collaborative observations.

## What is POLIS Provider?
A POLIS Provider is a site, that lists observing sites and strictly complies to the POLIS Standard (formats) and query APIs. To be a valid POLIS Provider, the site must only implement the first level of services. Implementation of the second and third level services is optional. There are 4 types of providers:

- `Public` sites confirm strictly to the POLIS standard, and provide APIs  at least in the JSON format (however XML is preferred for production sites). The site MUST list all known observatories (Earth and Solar system).
- `Private` sites are used locally by different organisations to support internal infrastructure or as a performance cache.
- `Mirror` sites are backups of a public sites and should be used only in the case that the public site is down for maintenance or due to technical issues.
- `Experimental` sites (as the name suggests), are used for implementing and testing new functionality or future unstable versions of the POLIS standard.

## Goals

- can list any type of facility: ground based, satellite, mobile, temporary (e.g. solar eclipse),...
- encourages the participation of amateur astronomers and educational organisations (schools, universities)
- open standard, mostly free to use for everyone, but some high-end services (weather monitoring, push notifications) could be available only for paying users to cover related hosting and service charges.
- can be used as datasource for mobile apps as well as for various web UIs and JSON/XML based APIs.
- supports API versions and of JSON and XML formats
- observatories can provide data either manually or with standard APIs
- distributed (no single point of failure). Different sites could provide complete or partial service.

## Further documentations

**Note:** the most current version of the documentation, sketches for new ideas, and different example files can be found in the `dev` branch.

...

## How to contribute
...

## History
The initial idea for a POLIS like protocol was first discussed at one of the HTN (Heterogeneous Network of Telescopes) conferences that took place about a decade ago in Tucson (AZ) and Göttingen (Germany). Initially an agent-based system that negotiates the exchange of observation time was discussed. The idea was to use RTML's `Dump` mode to describe the current status and capabilities of an observatory and to build a new negotiation protocol.

Around 2012 the [StarCluster](www.starcluster.app) team developed a very primitive prototype that was able to exchange status information between two imaginary observatories, however further development did not take place.

The idea for such a protocol was reborn in early 2019 when the StarCluster team started working on a new package of astronomy applications. In September 2020 [ASA](https://www.astrosysteme.com) and StarCluster worked together on a joined  bid for a new robotic telescope and it was during this period when the decision was made to start a new open source project with the goal to create a protocol and database of modern observatories, which monitor and report their status, and to allow individual sites to negotiate automatically or with human support for observation times and joined observation schedules.

Rick Hessman, University of Göttingen (Germany) coined the name POLIS and introduced the StarCluster team to the work of Rachel Street, who independently developed a database for monitoring observatory statuses.

In November 2020 the ASTRO-Polis project was created on GitHub.