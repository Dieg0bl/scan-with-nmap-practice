<!-- hide -->
# Scan ports with nmap

> By [@rosinni](https://github.com/rosinni) at [4Geeks Academy](https://4geeksacademy.co/)

[![build by developers](https://img.shields.io/badge/build_by-Developers-blue)](https://4geeks.com)
[![build by developers](https://img.shields.io/twitter/follow/4geeksacademy?style=social&logo=twitter)](https://twitter.com/4geeksacademy)

*Estas instrucciones están [disponibles en Español](https://github.com/breatheco-de/scan-with-nmap-practice/blob/main/README.es.md)*

### Before you start...

> We need you! These exercises are built and maintained in collaboration with contributors such as yourself. If you find any bugs or misspellings please contribute and/or report them.

<!-- endhide -->

## 📋 Project Purpose

This project is designed to teach network security fundamentals through hands-on practice with Nmap (Network Mapper). Students will learn to:

- Perform network reconnaissance and vulnerability assessment
- Identify active hosts and open ports on target systems
- Discover running services and their versions
- Search for potential security vulnerabilities
- Generate professional vulnerability reports
- Understand network security weaknesses and their implications

## 🛠️ Technologies Used

- **Nmap** - Network scanning and security auditing tool
- **Kali Linux** - Penetration testing and security auditing distribution (scanning machine)
- **Debian Linux** - Target operating system for vulnerability assessment
- **Bash/Shell** - Command-line interface for executing scans
- **Virtual Machines** - Virtualization technology for safe testing environment
- **CVE Databases** - Public vulnerability databases (NVD, CVE Details, Exploit-DB, Vulners)

## 🚀 How to Install and Run

### Prerequisites
* Virtual machine with Kali Linux (Scanning machine)
* Virtual machine with Debian (Target machine)
* Basic knowledge of Linux command line
* Network connectivity between both machines

### Installation

### Installation

1. **Set up your virtual machines:**
   - Ensure both Kali Linux and Debian VMs are running
   - Configure network connectivity between machines
   - Note the IP address of your Debian target machine

2. **Install Nmap on Kali Linux (if not already installed):**
   ```bash
   sudo apt-get update
   sudo apt-get install nmap
   ```

3. **Clone this repository:**
   ```bash
   git clone https://github.com/[your-username]/scan-with-nmap-practice.git
   cd scan-with-nmap-practice
   ```

### Execution Steps

## 📝 Practice Instructions

### Getting Started

1. **Fork this repository:**
   * Open this URL: https://github.com/breatheco-de/scan-with-nmap-practice
   * Click the Fork button to create a copy in your GitHub account

   ![fork button](https://github.com/4GeeksAcademy/4GeeksAcademy/blob/master/site/src/static/fork_button.png?raw=true)

2. **Clone your forked repository:**
   ```bash
   git clone https://github.com/[your-username]/scan-with-nmap-practice.git
   cd scan-with-nmap-practice
   ```

### Step 1: Scanning with Nmap

On the Kali machine, we will perform a scan with Nmap to discover active hosts and open ports on a network or a specific device.

- [ ] **Install Nmap (if not installed):**
```bash
sudo apt-get install nmap
```

- [ ] **Basic scan of target (Replace <debian_IP> with the Debian machine's IP):**
```bash
nmap <IP_debian>
```

### Step 2: Enumerate Ports and Verify Services
After performing the scan, Nmap will provide a list of open ports and the services operating on those ports.

- [ ] **Scan ports and services:**
```bash
nmap -sV <debian_IP>
```
> This option (-sV) allows detection of the version of the service operating on each port.

- [ ] **Detailed scan and vulnerability search:**
```bash
nmap -sV --script=vuln <debian_IP>
```
> The option (--script=vuln) runs Nmap's built-in vulnerability detection scripts.

### Step 3: Document Vulnerabilities Associated with Services

- [ ] **Note the Services and Their Versions:**
From the scan results, take note of the services and their versions. For example:
    * Apache 2.4.7
    * OpenSSL 1.0.1f
    * OpenSSH 6.6.1p1

- [ ] **Search for Vulnerabilities in Public Databases:**
Use public vulnerability databases to find information about the detected services. The most common sources are:
    * NVD (National Vulnerability Database): https://nvd.nist.gov/
    * CVE Details: https://www.cvedetails.com/
    * Exploit Database: https://www.exploit-db.com/
    * Vulners: https://vulners.com/

> 💡Example: For the Apache 2.4.7 service, go to the NVD page: https://nvd.nist.gov/ and enter "Apache 2.4.7" in the search bar.

- [ ] **Document the vulnerabilities in a structured manner.** Here is an example of how to document a vulnerability:

![vulnerability report](https://github.com/breatheco-de/scan-with-nmap-practice/blob/main/assets/report-vul.png?raw=true)

## 📤 Delivery

* Upload your vulnerability report in `.pdf` format to the root of your forked repository with the name `vulnerability-report.pdf`.
* Ensure your report includes:
  - Identified services and versions
  - CVE numbers and descriptions
  - Risk assessment for each vulnerability
  - Recommendations for remediation

## 📚 Additional Resources

- [Nmap Official Documentation](https://nmap.org/docs.html)
- [National Vulnerability Database](https://nvd.nist.gov/)
- [CVE Details](https://www.cvedetails.com/)
- [Exploit Database](https://www.exploit-db.com/)
- [Network Security Best Practices](https://www.nist.gov/cybersecurity)
