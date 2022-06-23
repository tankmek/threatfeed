![Hits](https://hitcounter.pythonanywhere.com/count/tag.svg?url=https%3A%2F%2Fgithub.com%2Ftankmekt%2Fthreatfeed)


# threatfeed
Rudimentary IP and URL threat feeds.

<!-- TABLE OF CONTENTS -->
## Table of Contents

* [Synopsis](#synopsis)
* [Description](#description)
* [License](#license)
* [Contact](#contact)

<!-- SYNOPSIS -->
## Synopsis
This repository is a collection of CSV files containing URL and IP addresses. The IP addresses represent source
hosts that have gained unauthorized access to at least one of several geographically distributed cowrie honeypots.
The URL feed represents locations that threat actors have been observed using to retrieve additional tools on at least
one of the honeypots.

The URL list has been deduped and any domains in the Alexa top one million removed.

This repository is also being used as a source for my [AlienVault OTX Pulse](https://otx.alienvault.com/pulse/62b111807cf993489def0c3b)

<!-- DESCRIPTION -->
## Description
The IP CSV is the exported lookup table from Splunk consisting of the following fields:

| Header      | Description |
| ----------- | ----------- |
| src_ip      | Source IP   |
| Country     | GeoIP location        |
| last_seen   | The last time the src_ip was seen in the dataset |
| first_seen  | The first time the src_ip was seen in the dataset|
| tor_exit_node | Checks if src_ip is listed as an exit node |
| sensor      | Integer indicating how many sensors have observed the src_ip |

The URL CSV is the exported lookup table from Splunk consisting of the following fields:

| Header      | Description  |
| ----------- | -----------  |
| indicator   | Observed URL |
| type        | type of indicator |
| last_seen   | The last time the URL was seen in the dataset |
| first_seen  | The first time the URL was seen in the dataset|
| ut_domain   | The extracted domain |
| sensor      | Integer indicating how many sensors have observed the URL |


## License
Distributed under the GNU General Public License v3.  
See `LICENSE` for more information.

<!-- CONTACT -->
## Contact

Michael Edie - [@tankmek](https://twitter.com/tankmek) - michael@edie.io
