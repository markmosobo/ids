<h1 align="center"> 
Slips v1.0.11
</h1>


# Table of Contents

- [Introduction](#introduction)
- [GUI](#graphical-user-interface)
- [Installation](#installation)
- [Configuration](#configuration)
- [Features](#features)


# Slips: Behavioral Machine Learning-Based Intrusion Prevention System


Slips is a powerful endpoint behavioral intrusion prevention and detection system that uses machine learning to detect malicious behaviors in network traffic. Slips can work with network traffic in real-time, PCAP files, and network flows from popular tools like Suricata, Zeek/Bro, and Argus. Slips threat detection is based on a combination of machine learning models trained to detect malicious behaviors, 40+ threat intelligence feeds, and expert heuristics. Slips gathers evidence of malicious behavior and uses extensively trained thresholds to trigger alerts when enough evidence is accumulated.



# Introduction
Slips is the first free software behavioral machine learning-based IDS/IPS for endpoints. The goal of this project was to offer a local IDS/IPS that leverages machine learning to detect network attacks using behavioral analysis. 


Slips is currently supported on Linux only.

Slips is Python-based and relies on [Zeek network analysis framework](https://zeek.org/get-zeek/) for capturing live traffic and analyzing PCAPs. and relies on
Redis >= 7.0.4 for interprocess communication.

# Graphical User Interface

To check Slips output using a GUI you can use the web interface 
or our command-line based interface Kalipso 

##### Web interface

    ./webinterface.sh

Then navigate to ```http://localhost:55000/``` from your browser.

<img src="https://raw.githubusercontent.com/stratosphereips/StratosphereLinuxIPS/develop/docs/images/web_interface.png" width="850px">

For more info about the web interface, check the docs: https://stratospherelinuxips.readthedocs.io/en/develop/usage.html#the-web-interface


##### Kalispo (CLI-Interface)

    ./kalipso.sh

<img src="https://raw.githubusercontent.com/stratosphereips/StratosphereLinuxIPS/develop/docs/images/kalipso.png" width="850px">


For more info about the Kalipso interface, check the docs: https://stratospherelinuxips.readthedocs.io/en/develop/usage.html#kalipso

---



# Installation

 * [Using install.sh](https://stratospherelinuxips.readthedocs.io/en/develop/installation.html#install-slips-using-shell-script)
 * [Manually](https://stratospherelinuxips.readthedocs.io/en/develop/installation.html#installing-slips-manually)

---

# Configuration
Slips has a [config/slips.conf] that contains user configurations for different modules and general execution.

* You can change the timewindow width by modifying the ```time_window_width``` parameter
* You can change the analysis direction to ```all```  if you want to see the attacks from and to your computer
* You can also specify whether to ```train``` or ```test``` the ML models 

* You can enable [popup notifications] of evidence, enable [blocking], [plug in your own zeek script] and more.

# Features
Slips key features are:

* **Behavioral Intrusion Prevention**: Slips acts as a powerful system to prevent intrusions based on detecting malicious behaviors in network traffic using machine learning.
* **Modularity**: Slips is written in Python and is highly modular with different modules performing specific detections in the network traffic.
* **Targeted Attacks and Command & Control Detection**: It places a strong emphasis on identifying targeted attacks and command and control channels in network traffic.
* **Traffic Analysis Flexibility**: Slips can analyze network traffic in real-time, PCAP files, and network flows from popular tools like Suricata, Zeek/Bro, and Argus.
* **Threat Intelligence Updates**: Slips continuously updates threat intelligence files and databases, providing relevant detections as updates occur.
* **Integration with External Platforms**: Modules in Slips can look up IP addresses on external platforms such as VirusTotal and RiskIQ.
* **Graphical User Interface**: Slips provides a console graphical user interface (Kalipso) and a web interface for displaying detection with graphs and tables.
* **Peer-to-Peer (P2P) Module**: Slips includes a complex automatic system to find other peers in the network and share IoC data automatically in a balanced, trusted manner. The P2P module can be enabled as needed.
* **Docker Implementation**: Running Slips through Docker on Linux systems is simplified, allowing real-time traffic analysis.
* **Detailed Documentation**: Slips provides detailed documentation guiding users through usage instructions for efficient utilization of its features.






# ids
