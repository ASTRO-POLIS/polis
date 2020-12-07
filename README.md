# POLIS - Public Observatory Location and Information Service


## What is POLIS?
As the name suggests, the Public Observatory Location and Information Service provides a directory type of distributed services (similar to DNS) listing astronomical observing sites across the world as well as satellites. Three levels of services are offered:

1. The Observatory Location and Information service describes the observing (observation?) Facilities. It is only updated on demand (automatically, or manually) when there are changes at the facility.
2. Currently known status changes and long-term night by night scheduling.
3. Real time status changes and observation scheduling, facilitates  observatory to observatory real time communication and collaborative observations.

## What is POLIS Provider?
A POLIS Provider is a site, that lists observing sites that strictly follow the APIs and formats defined by the POLIS standard. To be a valid POLIS Provider, the site must only implement the first level of services. Implementation of the second and third level services is optional. There are 4 types of providers:

- `Public` sites confirm strictly to the POLIS standard, and provide APIs  at least in the JSON format (however XML is preferred for production sites). The site MUST list all known observing (observation) sites.
- `Private` sites are used locally by different organisations to support internal infrastructure or as a performance / traffic cache.
- `Mirror` sites are backups of a public site and should be used exclusively in the case the public site is down for maintenance or due to technical issues.
- `Experimental` sites (as the name suggests), are used for implementing and testing new functionality or future unstable versions of the POLIS standard.

## Goals

- can list any type of facility: ground based, satellite, mobile, temporary (e.g. solar eclipse),...
- encourages the participation of amateur astronomers and educational organisations (schools, universities)
- open standard, mostly free to use for everyone, but some high-end services (weather monitoring, push notifications) could be available only for paying users to cover related hosting and service charges.
- can be used as datasource for mobile apps as well as for various web UIs and JSON/XML based APIs.
- supports API versions and (of?) JSON and XML formats
- observatories can provide data either manually or with standard APIs
- distributed (no single point of failure). Different sites could provide complete or partial service.

## APIs

### Level 1: static (no query facilities) directory of observing facilities

#### POLIS Provider Directory
A complete list of known POLIS providers, including their root URL, last update time, service level, and standard supporting version(s), and format (e.g. XML, JSON).

#### Observing Sites Directory

#### Observing Site

### Level 2:

### Level 3: 

## General notes and comments

### Note on IDs

Most APIs will involve unique (within POLIS) IDs. To avoid any privacy issues and tracing by bad actors, all UUIDs should be random (version 4 as defined by other UUID standards). The Swift-polis package generates random UUIDs by default.

Within an Observing Site all Observatories and/or instruments can have optional unique IDs. Globally they could be identified using the following convention: `ObservingSiteID:::LocalID`

### Bootstrapping a new POLIS provider
In order to launch a new POLIS site, data should be initialised using a known site. This project maintains a list of root URLs to well known sites that could be used to read the initial information. It is strongly reccomended, that the administrators of a new POLIS provider announce the new provider to at least one of the known sites in order to be made available to the network of providers. Currently, there is only a single know POLIS provider: `polis.observer`.

### Data formats
Both JSON and XML data formats are supported by POLIS because of its richness, support for schema, and schema validation. It is recommended to use XML whenever possible.

### Date and Time formats

All Date and Time formats must be in ISO8601 format and must be in UTC

# History
The initial idea for a POLIS like protocol was first discussed at one of the HTN (Heterogeneous Network of Telescopes) conferences that took place about a decade ago in Tucson (AZ) and Göttingen (Germany). Initially an agent-based system that negotiates the exchange of observation time was discussed. The idea was to use RTML's `Dump` mode to describe the current status and capabilities of an observatory and to build a new negotiation protocol.

Around 2012 the [StarCluster](www.starcluster.app) team developed a very primitive prototype that was able to exchange status information between two imaginary observatories, however further development did not take place.

The idea for such a protocol was reborn in early 2019 when the StarCluster team started working on a new package of astronomy applications. In September 2020 [ASA](https://www.astrosysteme.com) and StarCluster worked together on a joined  bid for a new robotic telescope and it was during this period when the decision was made to start a new open source project with the goal to create a protocol and a database of modern observatories, to monitor and report their status, and to allow individual sites to negotiate automatically or with human support for observation times and joined observation schedules.

Rick Hessman at Göttingen University (Germany) coined the name POLIS and introduced the StarCluster team to the work of Rachel Street, who independently developed a database for monitoring observatory statuses.

In November 2020 the ASTRO-Polis project was created on GitHub.
