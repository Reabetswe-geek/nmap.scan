## Achieved
- Baic scans were performed on localhose, though most scanned ports were in ignored states, indicaticating that no active services were exposed on the target system
- External test servers were done to identify open,closed and filtered ports
- The scan revealed open ports on the target system, indicating active services such as SSH and HTTP, which could represent potential entry points
- Due to network restrictions in WSL, TCP Connect scan (-sT) with host discovery disable (-Pn) was used to successfully identify open ports on the target system 
- SYN scan (-sS) was attempted but failed due to environment limitations in WSL, higlighting restrictions in raw packet handling
- TCP Connect scan (-sT) was used as a reliable alternative
