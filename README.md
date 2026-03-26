## Achieved
- Baic scans were performed on localhose, though most scanned ports were in ignored states, indicaticating that no active services were exposed on the target system
- External test servers were done to identify open,closed and filtered ports
- The scan revealed open ports on the target system, indicating active services such as SSH and HTTP, which could represent potential entry points
- Due to network restrictions in WSL, TCP Connect scan (-sT) with host discovery disable (-Pn) was used to successfully identify open ports on the target system 
- SYN scan (-sS) was attempted but failed due to environment limitations in WSL, higlighting restrictions in raw packet handling
- TCP Connect scan (-sT) was used as a reliable alternative

## -sV output
- Service and detection was performed to identify software running on open ports, enabling further vulnerability assessment

## OS detection
- OS detection was attempted using nmap to identify the target system. Due to environmental limitations, results may vary, demonstrating real-work scanning constraints

## Aggressive output
- An aggressive scan (-A) was performed to combine service detection, OS fingerprinting, and script-based analysis, providing a comprehensive view of the target system/
- Aggressive scanning revealed additional information through NSE scripts, including HTTP TITLE and server headers.
- This allowed further fingerprinting of the target system, identifying a likely apache web server running on a Linux-based system.
