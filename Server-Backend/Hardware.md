# Specifications
These are the specifications for the hardware being used when I am providing the tech for a speedrun marathon:

- Restream Machine
    - Used for stream broadcast
    - Accessed via NoMachine or Parsec; uses VPS as a repeater for NoMachine
    - Intel i7-6700 3.40 GHz
    - NVIDIA Quadro P400
    - Windows 10 Professional / Linux Pop_OS 22.04 LTS (Ubuntu)
- Virtual Private Server
    - Only public facing device
    - May be used to host web apps such as:
        - Sync timer
        - Producer emergency "go to break screen" button if something goes horribly wrong
    - 1 vCPU
    - 1 GB RAM
- NodeCG Speedcontrol Server
    - Used only for hosting NodeCG
    - Accessed via web browser; NGINX through VPS + Tailscale
    - Raspberry Pi 3B+
    - Raspberry Pi OS (Raspbian Debian 11)
