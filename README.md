<div id="top"></div>

<div align="center">
	<a href="https://github.com/Link-Wolf/minitalk" title="Go to GitHub repo"><img src="https://img.shields.io/static/v1?label=Link-Wolf&message=minitalk&color=blue&logo=github&style=for-the-badge" alt="Link-Wolf - minitalk"></a>
	<a href="https://"><img src="https://img.shields.io/badge/42_grade-125_%2F_100-2ea44f?style=for-the-badge" alt="42 grade - 125 / 100"></a>
	<a href="https://"><img src="https://img.shields.io/badge/Year-2022-ffad9b?style=for-the-badge" alt="Year - 2022"></a>
	<a href="https://github.com/Link-Wolf/minitalk/stargazers"><img src="https://img.shields.io/github/stars/Link-Wolf/minitalk?style=for-the-badge&color=yellow" alt="stars - minitalk"></a>
	<a href="https://github.com/Link-Wolf/minitalk/network/members"><img src="https://img.shields.io/github/forks/Link-Wolf/minitalk?style=for-the-badge&color=lightgray" alt="forks - minitalk"></a>
	<a href="https://github.com/Link-Wolf/minitalk/issues"><img src="https://img.shields.io/github/issues/Link-Wolf/minitalk?style=for-the-badge&color=orange" alt="issues - minitalk"></a>
	<a href="https://www.apple.com/macos/" title="Go to Apple homepage"><img src="https://img.shields.io/badge/OS-macOS-blue?logo=apple&logoColor=white&style=for-the-badge&color=9cf" alt="OS - macOS"></a>
</div>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a>
    <img src="https://www.42mulhouse.fr/wp-content/uploads/2022/06/logo-42-Mulhouse-white.svg" alt="Logo" width="192" height="80">
  </a>

  <h3 align="center">Minitalk</h3>

  <p align="center">
	  <em>Ping ? Pong !</em><br/>
    Small server and client using UNIX signals
    <br />
    <br />
    <a href="https://github.com/Link-Wolf/minitalk/issues">Report Bug</a>
    ·
    <a href="https://github.com/Link-Wolf/minitalk/issues">Request Feature</a>
  </p>
</div>


<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

<div align="center">
  <a>
    <img src="https://media.discordapp.net/attachments/453159761639112706/998567627825889310/unknown.png" alt="minitalk header">
  </a>
</div>

This project is focused on our first server and client to send/receive data (string) only by using `SIGUSR1` and `SIGUSR2` UNIX signals <br />
- The server must print its `PID` when launched
- The client must be launched by specifying the server `PID` and the string to send
- The server must be able to receive data from different clients without being rebooting

As bonuses features : <br />
- The server should answer when all the data is successfully received
- The client should print the answer sent by the server
- Both client and server should support Unicode characters

To do all of this, I used both <code>SIGUSR1</code> & <code>SIGUSR2</code> signals as binary instructions to encode and decode the informations

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- GETTING STARTED -->
## Getting Started

Because they're simple C programs, there isn't much to say here

### Prerequisites

Having a C compiler like cc, gcc or clang

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/Link-Wolf/minitalk.git
   ```
2. Compile minitalk
   ```sh
   cd minitalk; make
   ```
3. Start the server
   ```sh
   ./server
   ```
4. Start the client in another terminal, by specify the server `PID` (printed by the server when started) and the data to send
   ```sh
   ./client 21502 "my awesome data"
   ```

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage

Test this minitalk with whatever you want, any-size strings, even with unicode !

#### Server
```sh
   ./server
```
Immediate output :
```sh
   21502
```
#### Client
```sh
   ./client 21502 "woaw it's working !"
```

### Output

#### Server
```
   woaw it's working !
```
#### Client
```
   > Your message has been correctly shreked to the server my dude ! \_ÒwÓ_/
```
*(Of course you can change the confirmation message)*

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

- [x] Add server answer
- [x] Add unicode support
- [x] Add back to top links

See the [open issues](https://github.com/Link-Wolf/minitalk/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#top">back to top</a>)</p>

<!-- CONTACT -->
## Contact

Mail : xxxxxxx@student.42mulhouse.fr

Project Link: [https://github.com/Link-Wolf/minitalk](https://github.com/Link-Wolf/minitalk)

<p align="right">(<a href="#top">back to top</a>)</p>
