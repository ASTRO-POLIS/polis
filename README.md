# POLIS - Public Observatory Location and Information Service


## What is POLIS?
As the name suggests, the Public Observatory Location and Information Service provides a directory type of distributed services (similar to DNS) listing astronomical observing sites across the world as well as satellites. There are three levels of services:

1. Observatory Location and Information service describes the observing facilities. It is updated only on demand (automatically, or manually) when there are changes in the facility.
1. Current known status changes and long-term night by night scheduling.
1. Real time status changes and observation scheduling, facilitation of observatory to observatory real time communication and collaborative observations.

To be listed, only the first level of services is required.

## Goals

- can list any type of facility: ground based, satellite, mobile, temporary (e.g. solar eclipse),...
- encourages the participation of amateur astronomers and educational organisations (schools, universities)
- open standard, mostly free to use for everyone, but some high-end services (weather monitoring, push notifications) could be available only for paying users to cover related hosting and service charges.
- can be used as datasource for mobile apps as well as various web UIs and JSON/XML based APIs.
- supports API versions and JSON and XML formats
- observatories could provide data either manually, or with APIs
- distributed (no single point of failure). Different sites could provide complete or partial service and only level 1 services is required.

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

Most APIs will involve unique (within POLIS) IDs. To avoid any privacy issues and tracing by bad actors, all UUIDs should be random (version 4 as defined by other UUID standards). Swift-polis package by default generates random UUIDs.

Within an Observing Site all Observatories and/or instruments could have an optional unique IDs. Globally they could be identified using the following convention: `ObservingSiteID:::LocalID`

### Bootstrapping a new POLIS provider
In order to launch a new POLIS site, data should be initialised using a known site. This project maintains a list of root URLs to well known sites that could be used to read the initial information. It is strongly suggested, that the administrators of a new POLIS provider announce the new provider to at least one of the known sites in order to be announced to the network of providers. Currently, there is only a single know POLIS provider: `polis.observer`.

### Data formats
Both JSON and XML data formats are supported by POLIS. Because of its richness, support for schema, and schema validation it is recommended to use XML whenever possible.

### Date and Time formats

All Date and Time formats must be in ISO8601 format and must be in UTC

# History
The initial idea for a POLIS like protocol was first discussed at one of the HTN (Heterogeneous Network of Telescopes) conferences that took place about a decade ago in Tucson (AZ) and Göttingen (Germany). Initially an agent-based system that negotiate the exchange of observation time was discussed.  The idea was to use RTML's `Dump` mode to describe the current status and capabilities of an observatory and to build a new negotiation protocol.

Around 2012 the [StarCluster](www.starcluster.app) team developed a very primitive prototype that was able to exchange status information between two imaginary observatories, but no further development took place.

The idea for such protocol was reborn in early 2019 when the StarCluster team started working on a new package of astronomy applications. In September 2020 [ASA](https://www.astrosysteme.com) and StarCluster worked together on a joined  bid for a new robotic telescope and it was during this period when the decision was made to start a new open source project with the goal to create a protocol and a database of modern observatories, monitor and report their status, and allow individual sites to negotiate automatically or with human support for observation time and joined observation schedules.

Rick Hessman at Göttingen University (Germany) coined the name POLIS and introduced the StarCluster team to the work of Rachel Street, who independently developed a database for monitoring observatory statuses.

In November 2020 the ASTRO-Polis project was created on GitHub.
