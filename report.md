# Nmap Network Scan report

## Target
scanme.nmap.org

-----

## Scan Methodology

The following Nmap techniques were used:

- TCP connect scan (-sT)
- Service & Version Detection (-sV)
- OS Detection (-O)
- Aggressive scan (-A)
- Host discovery disabled (-Pn) due to network restrictions

-----

## Open Ports Identified

|Ports| State | Service |
-------------------------
|22   | Open  |  SSH    |
|80   | Open  |  HTTP   |

-----

## Service & Version detection

- Port 22: SSH service detected
- Port 80: HTTP service detected

------

## OS Detection
Nmap returned:
Linux 4.15 -5.8 (92% confidence)

This suggests the target is likely running a Linux-based operating system.

------

## NSE Script Findings

Aggressive scanning revealed:

- HTTP Title: Identifies the webpage
- HTTP Server header: Indicates Apache web server

------

## Analysis

The target system appears to be:

- A linux-based server
- Running SSH (remote access)
- Running a web server (Apache)

These exposed services represent potential attack surfaces.

-------

## Limitations

- SYN scan (-sS) was unreliable due to WSL environment restrictions
- TCP Connect scan (-sT) was used as a reliable alternative
- Some scans required limiting ports for stability

-------

## Conclusion

This assessment demonstrates the ability to;

- Perform network reconnaissance
- Identify open ports and services
- Conduct OS fingerprinting
- Extract additional intelligence using NSE script
- Adapt scanning techniques based on environment limitations
