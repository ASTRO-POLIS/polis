# Introduction to POLIS APIs

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
