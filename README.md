# Utkuici - Nessus Automation

## Description

Today, with the spread of information technology systems, investments in the field of cyber security have increased to a great extent. Vulnerability management, penetration tests and various analyzes are carried out to accurately determine how much our institutions can be affected by cyber threats. With Tenable Nessus, the industry leader in vulnerability management tools, an IP address that has just joined the corporate network, a newly opened port, exploitable vulnerabilities can be determined, and a python application that can work integrated with Tenable Nessus has been developed to automatically identify these processes.

## Features

- Finding New IP Address
- Finding New Port
- Finding New Exploitable Vulnerability

## Installation

git clone https://github.com/anil-yelken/Nessus-Automation
cd Nessus-Automation
sudo pip3 install requirements.txt

## Usage

The SIEM IP address in the codes should be changed.

In order to detect a new IP address exactly, it was checked whether the phrase "Host Discovery" was used in the Nessus scan name, and the live IP addresses were recorded in the database with a timestamp, and the difference IP address was sent to SIEM. The contents of the hosts table were as follows:

Usage: python finding-new-ip-nessus.py

<img src="https://github.com/anil-yelken/Nessus-Automation/blob/main/new_host.png">

By checking the port scans made by Nessus, the port-IP-time stamp information is recorded in the database, it detects a newly opened service over the database and transmits the data to SIEM in the form of "New Port:" port-IP-time stamp.
The result observed by SIEM is as follows:

Usage: python finding-new-port-nessus.py

<img src="https://github.com/anil-yelken/Nessus-Automation/blob/main/new_port.png">

In the findings of vulnerability scans made in institutions and organizations, primarily exploitable vulnerabilities should be closed. At the same time, it records the vulnerabilities in the database that can be exploited with metasploit in the institutions and transmits this information to SIEM when it finds a different exploitable vulnerability on the systems.
Exploitable vulnerabilities observed by SIEM:

Usage: python finding-exploitable-service-nessus.py

<img src="https://github.com/anil-yelken/Nessus-Automation/blob/main/exploitable.png">

## Contact

https://twitter.com/anilyelken06

https://medium.com/@anilyelken



