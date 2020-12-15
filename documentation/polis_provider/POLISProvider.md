# POLIS Provider

This document describes how to identify a site as POLIS provider.

Every POLIS provider **must** implement one of the following links (or preferably - both):

- `https://polis.provider.site/polis/polis.json`
- `https://polis.provider.site/polis/polis.xml`

Each of these resources (dynamic or static) **must** contain the following information:

- Name: The name of the provider, like `National Astronomical Observatory`
- Optional description
- UID: a UUID of the provider. It is recommended the UUID to be random (e.g. UUID version 4). Example for such ID is `F7814DEE-AC5D-433B-A9FA-85A37E716237`
- Last update in ISO8601 format (e.g. `"2019-02-06T00:35:01.746Z"`)
- Supported Protocol Levels: possible values are 1 .. 3. See main README.md for more
- Supported API Versions: an array of strings representing Semantic Versions (should be sorted), (e.g. `["1.0", "1.2", 2.0"]`.
- Supported Data Types: currently only `xml` and `json` are supported.
- Provider Type: currently supported types are `public`, `private`, `mirror`, and `experimental` where:
	- `public` is an officially publicly available service that fully supports at lease Level 1 POLIS protocol. Could be accessible for free by anyone.
	- `private` marks a site for private use that could have most of the information behind password protected user accounts.
	- `mirror` marks a provider that replicates another POLIS provider as backup service. Should be queried only if the mirrored site is unreachable. The `providerType` value should be in the following format: `mirror:::F7814DEE-AC5D-433B-A9FA-85A37E716237` where the UUID represents the iD of the mirrored site.
	- `experimental` marks an experimental provider, perhaps in the process of initial construction, or playing with future versions of POLIS.

