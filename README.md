<!-- hide -->
# Scan ports with nmap

> By [@rosinni](https://github.com/rosinni) at [4Geeks Academy](https://4geeksacademy.co/)

[![build by developers](https://img.shields.io/badge/build_by-Developers-blue)](https://4geeks.com)
[![build by developers](https://img.shields.io/twitter/follow/4geeksacademy?style=social&logo=twitter)](https://twitter.com/4geeksacademy)

*Estas instrucciones están [disponibles en Español](https://github.com/Dieg0bl/scan-with-nmap-practice/blob/main/README.es.md)*

### Before you start...

> We need you! These exercises are built and maintained in collaboration with contributors such as yourself. If you find any bugs or misspellings please contribute and/or report them.

<!-- endhide -->

## 🌱 How to start a project?

In this practice, we will learn how to use Nmap, a widely recognized open-source tool for network analysis and security. With Nmap, we will perform scans on a target machine (in this case, a Debian machine) from a Kali Linux machine.

We will identify active hosts, open ports on the network, and which services are operating on those ports. This will allow us to search for possible vulnerabilities in the detected services and understand the security weaknesses that may exist in the network.

### Requirements
* Virtual machine with Kali Linux (Scannig machine)
* Virtual machine with Debian (Target machine)

## 📝 Instructions

* Open this URL and fork the repository https://github.com/Dieg0bl/scan-with-nmap-practice

 ![fork button](https://github.com/4GeeksAcademy/4GeeksAcademy/blob/master/site/src/static/fork_button.png?raw=true)

A new repository will be created in your account.

* Clone the newly created repository into your localhost computer.
* Once you have cloned successfully, follow the steps below carefully, one by one.

### Step 1: Scanning with Nmap

On the Kali machine, we will perform a scan with Nmap to discover active hosts and open ports on a network or a specific device.

- [ ] Install Nmap (if not installed):
```bash
sudo apt-get install nmap
```

- [ ] Basic scan of a target (Replace <debian_IP> with the Debian machine's IP):
```bash
nmap <IP_debian>
```

### Step 2: Enumerate Ports and Verify Services
After performing the scan, Nmap will provide a list of open ports and the services operating on those ports.

- [ ] Scan ports and services:
```bash
nmap -sV <debian_IP>
```
> This option (-sV) allows detection of the version of the service operating on each port.

- [ ] Detailed scan and vulnerability search:
```bash
nmap -sV --script=vuln <debian_IP>
```
> The option (--script=vuln) runs Nmap's built-in vulnerability detection scripts.

### Step 3: Document Vulnerabilities Associated with Services

- [ ] Note the Services and Their Versions
From the scan results, take note of the services and their versions. For example:
    * Apache 2.4.7
    * OpenSSL 1.0.1f
    * OpenSSH 6.6.1p1

- [ ] Search for Vulnerabilities in Public Databases
Use public vulnerability databases to find information about the detected services. The most common sources are:
    * NVD (National Vulnerability Database): https://nvd.nist.gov/
    * CVE Details: https://www.cvedetails.com/
    * Exploit Database: https://www.exploit-db.com/
    * Vulners: https://vulners.com/

> 💡Example: For the Apache 2.4.7 service, go to the NVD page: https://nvd.nist.gov/ and enter "Apache 2.4.7" in the search bar.

- [ ] Document the vulnerabilities in a structured manner. Here is an example of how to document a vulnerability:

![vulnerability report](https://github.com/Dieg0bl/scan-with-nmap-practice/blob/main/assets/report-vul.png?raw=true)

## Delivery

* In the root of the forked project, upload the report in `.pdf` format with the name `vulnerability-report.pdf`.
