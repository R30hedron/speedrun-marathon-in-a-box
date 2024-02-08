### Disclaimer
Note that I am not an IT professional nor am I trained in proper information security. The following guide is more for my own documentation and should not be taken as gospel by anyone and is meant for informational purposes only.
If you are actually an IT pro or in infosec, feel free to message me or suggest changes to the below.

# Specifications
These are the specifications for the hardware being used when I am providing the tech for a speedrun marathon:

- Restream Machine
    - Used for stream broadcast
    - Accessed 
    - Intel i5-6500 3.20 GHz
    - NVIDIA Quadro P400
    - Windows 10 Professional / Linux Pop_OS 22.04 LTS (Ubuntu)
- Virtual Private Server
    - Used for hosting a realtime clock timecode sync timer and for external network access
    - Only public facing device; accessed via web browser
    - 1 vCPU
    - 1 GB RAM
- NodeCG Speedcontrol Server
    - Used only for hosting NodeCG
    - Accessed via web browser; NGINX through VPS + Tailscale
    - Raspberry Pi 3B+
    - Raspberry Pi OS (Raspbian Debian 11)
