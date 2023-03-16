<div id="top"></div>

<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/pharm-it-de/netdata-pharmit">
    <img src="https://user-images.githubusercontent.com/1153921/95268672-a3665100-07ec-11eb-8078-db619486d6ad.png" alt="Logo">
  </a>

<h3 align="center">Netdata - Pharm-IT</h3>

  <p align="center">
    Pre-configured Netdata Agent by Pharm-IT for monitoring use.
    <br />
    <a href="https://learn.netdata.cloud/docs/"><strong>Explore the docs »</strong></a>
    <br />
    <a href="https://github.com/pharm-it-de/netdata-pharmit/issues">Report Bug</a>
    ·
    <a href="https://github.com/pharm-it-de/netdata-pharmit/issues">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

This is a pre-configured `Netdata Agent` by Pharm-IT for monitoring use. Despite the pre-configured example from `netdata.cloud` it uses a custom network `netdata`. This docker network will be created by the `docker-compose.yml` file. In the standard cloud-init script the `netdata` network will be allowed to communicate with the host system by the ufw firewall settings (https://askubuntu.com/a/903358).

These settings are necessary to send, for example, metrics of the `Docker Engine` via the [metrics endpoint](https://docs.docker.com/config/daemon/prometheus/).

<p align="right">(<a href="#top">back to top</a>)</p>



### Built With

* [netdata](https://www.netdata.cloud/)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

Because the project is dockerized, you can run the following command to start the `Netdata Agent` instance.

### Installation

1. Install [Docker](https://docs.docker.com/engine/install/) and [Docker Compose](https://docs.docker.com/compose/install/)
2. Clone the repo
   ```sh
   git clone https://github.com/pharm-it-de/netdata-pharmit.git
   ```
3. Create the `.env`-file
   ```sh
    # Name of the instance, will be display in netdata.cloud as indicator
    NETDATA_HOSTNAME=<name-of-the-instance>

    # login to netdata.cloud and get token from "Connect Nodes" > "Docker" > "NETDATA_CLAIM_TOKEN"
    NETDATA_CLAIM_TOKEN=<token from netdata.cloud>
    
    # login to netdata.cloud and get token from "Connect Nodes" > "Docker" > "NETDATA_CLAIM_URL"
    NETDATA_CLAIM_URL=https://app.netdata.cloud
    
    # optional: login to netdata.cloud and get token from "Connect Nodes" > "Docker" > "NETDATA_CLAIM_ROOMS"
    # NETDATA_CLAIM_ROOMS=<UUID of the room>
   ```
4. Run the docker containers
   ```sh
   docker-compose up -d
   ```

<p align="right">(<a href="#top">back to top</a>)</p>


<!-- CONTACT -->
## Contact

Project Link: [https://github.com/pharm-it-de/netdata-pharmit](https://github.com/pharm-it-de/netdata-pharmit)

<p align="right">(<a href="#top">back to top</a>)</p>


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/pharm-it-de/netdata-pharmit.svg?style=for-the-badge
[contributors-url]: https://github.com/pharm-it-de/netdata-pharmit/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/pharm-it-de/netdata-pharmit.svg?style=for-the-badge
[forks-url]: https://github.com/pharm-it-de/netdata-pharmit/network/members
[stars-shield]: https://img.shields.io/github/stars/pharm-it-de/netdata-pharmit.svg?style=for-the-badge
[stars-url]: https://github.com/pharm-it-de/netdata-pharmit/stargazers
[issues-shield]: https://img.shields.io/github/issues/pharm-it-de/netdata-pharmit.svg?style=for-the-badge
[issues-url]: https://github.com/pharm-it-de/netdata-pharmit/issues
[license-shield]: https://img.shields.io/github/license/pharm-it-de/netdata-pharmit.svg?style=for-the-badge
[license-url]: https://github.com/pharm-it-de/netdata-pharmit/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/company/pharm-it-de
