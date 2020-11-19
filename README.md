# POLIS - Public Observatory Location and Information Service


## What is POLIS?
As the name suggests, the Public Observatory Location and Information Service provides a directory type of distributed services (similar to DNS) listing astronomical observing sites across the world as well as satellites. There are three levels of services:

1. Observatory Location and Information service describes the observing facilities.It is updated only on demand (automatically, or manually) when there are changes in the facility.
1. Current known status changes and long-term night by night scheduling.
1. Real time status changes and observation scheduling, facilitation of observatory to observatory real time communication and collaborative observations.

To be listed, only the first level of services is required.

The name was suggested by Rick Hessman at Göttingen University (Germany) and the service is developed and made publicly available by the [StarCluster](www.starcluster.app) team. The idea for the service has its origins with the RTML standard. The first experimental implementation was developed around 2012 based on RTML Dump and was inspired by discussions at several VO related conferences during 2007-2009.

## Goals

- can list any time of facility: ground based, satellite, mobile, temporary (e.g. solar eclipse),...
- encourages the participation of amateur astronomers and educational organisations (schools, universities)
- open standard, but some high-end services (weather monitoring, push notifications) could be available only for paying users to cover related hosting and service charges.
- can be used as datasource for mobile apps as well as various web UIs and JSON/XML based APIs.
- supports API versions
- observatories could provide data either manually, or with APIs
- distributed (no single point of failure). Different sites could provide complete or partial service and only level 1 services is required.

## General notes and comments

### Note on IDs

Most APIs will involve unique (within POLIS) IDs. To avoid any privacy issues and tracing by bad actors, all UUIDs should be random (version 4 as defined by other UUID standards). Swift-polis package by default generates random UUIDs.