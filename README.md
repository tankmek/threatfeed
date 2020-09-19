![Hits](https://hitcounter.pythonanywhere.com/count/tag.svg?url=https%3A%2F%2Fgithub.com%2Ftankmekt%2Fthreatfeed)


# threatfeed
A rudimentary IP threat feed.

<!-- TABLE OF CONTENTS -->
## Table of Contents

* [Synopsis](#synopsis)
* [License](#license)
* [Contact](#contact)

<!-- SYNOPSIS -->
## Synopsis
This project is a CSV file containing host IP addresses that have gained unauthorized access
to at least one of several geographically distributed cowrie honeypots.  

The CSV is the exported lookup table from Splunk consisting of the following fields:

| Header      | Description |
| ----------- | ----------- |
| src_ip      | Source IP   |
| Country     | GeoIP location        |
| last_seen   | The last time the src_ip was seen in the dataset |
| first_seen  | The first time the src_ip was seen in the dataset|
| tor_exit_node | Checks if src_ip is listed as an exit node |
| sensor      | Integer indicating how many sensors have seen the src_ip |


## License
Distributed under the GNU General Public License v3.  
See `LICENSE` for more information.

<!-- CONTACT -->
## Contact

Michael Edie - [@tankmek](https://twitter.com/tankmek) - michael@edie.io
