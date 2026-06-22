# Windows Release – v1.0.0

fsociety Pentesting Tools Installer for Windows
Created by azooz64

The first official, stable Windows release of the fsociety framework – a menu-driven
toolchain installer that puts 80+ essential pentesting utilities right at your fingertips.
No more memorising package manager commands, no more scouring GitHub READMEs for
installation steps. Just open, pick a tool, and hit Install.

---

## What is this?

fsociety is a cross‑platform Python script that acts as a central hub for downloading
and installing the most popular security tools. It wraps multiple package managers
(winget, Chocolatey, pip, git) and direct downloads into a single, easy‑to‑navigate
terminal interface.

This release is the Windows edition, purpose‑built for Windows 10/11. It requires
no elevated privileges, no configuration, and no command‑line knowledge beyond
double‑clicking a file.

---

## Key Features

- **14 categories** covering every phase of a penetration test:
  Information Gathering, Vulnerability Analysis, Exploitation, Wireless Attacks,
  Forensics, Web Applications, Stress Testing, Sniffing & Spoofing, Password Attacks,
  Maintaining Access, Hardware Hacking, Reverse Engineering, Reporting Tools,
  and a special "Extra New Tools" section by azooz64.

- **80+ tools** ready to install with one keypress, including:
  Nmap, Wireshark, Metasploit, John the Ripper, Hydra, Hashcat, Aircrack-ng,
  Burp Suite, OWASP ZAP, Ghidra, SQLmap, Nikto, Nuclei, BeEF, SET, WPScan,
  Amass, Subfinder, httpx, FFUF, Sherlock, PhoneInfoga, Holehe, and many more.

- **Intelligent multi‑method installer**
  For each tool, the script tries up to four different installation strategies:
  1. winget (built into Windows 10/11)
  2. Chocolatey (if installed)
  3. Direct download of the official installer / portable zip
  4. git clone + pip install (for Python‑based tools)
  The first method that succeeds wins – you don’t have to worry about what is or
  isn’t available on your system.

- **Real‑time detection**
  The script scans your system after every install and updates the status immediately.
  You’ll never see "Installed" for a tool that isn’t actually there, and you’ll never
  waste time reinstalling something that is.

- **Classic hacker aesthetic**
  The iconic fsociety ASCII banner, colour‑coded prompts, and clean menu structure
  make you feel right at home in the terminal.

- **Zero dependencies (almost)**
  The script itself uses only the Python standard library. Git is recommended for
  tools that clone from repositories, but the script will skip git‑based methods
  gracefully if git isn’t found.

- **Extensible**
  Adding a new tool is as simple as inserting a few lines into a dictionary.
  The framework is built to be customised.

---

## Requirements

- **Windows 10 or 11**
- **Python 3.11 or 3.12** (download from https://python.org)
  Python 3.13+ is not recommended – many pentesting tools are not yet compatible.
- **Git** (optional, but highly recommended – download from https://git-scm.com)
- An internet connection (tools are downloaded on demand)

No admin rights are required for most tools. The script installs everything to
your user directory.

---

## How to use

1. Download `fsociety.py` from this release.
2. **Double‑click the file** – it will open in a terminal window automatically.
3. The main menu appears. Type the number of the category you want and press Enter.
4. Choose a tool from the list and hit **I** to install it.
5. Watch the installer do its work. When it’s finished, the tool will show as
   "Installed" immediately.

That’s it. No command lines, no manual downloads, no admin popups.

---

## Tools included (full list)

### Information Gathering
Nmap, whois, dnsrecon, dnsmap, theHarvester, recon-ng, Sublist3r, Amass,
Subfinder, httpx, gau, waybackurls

### Vulnerability Analysis
Nikto, Nuclei, SQLmap, Commix, XSStrike, Dalfox

### Exploitation Tools
Metasploit, BeEF, SET (Social‑Engineer Toolkit), RouterSploit, WPScan

### Wireless Attacks
Aircrack-ng, Reaver, Kismet, Wifite

### Forensic Tools
Autopsy, Binwalk, Volatility

### Web Applications
Burp Suite Community, OWASP ZAP, SQLmap (again), WhatWeb, WPScan (again), CMSeeK

### Stress Testing
hping3, Slowloris, LOIC

### Sniffing & Spoofing
Wireshark, tcpdump, Bettercap

### Password Attacks
John the Ripper, Hydra, Hashcat, Crunch, CeWL

### Maintaining Access
Netcat, PowerShell Empire

### Hardware Hacking
Arduino IDE

### Reverse Engineering
Ghidra, Radare2

### Reporting Tools
Dradis

### Extra New Tools (by azooz64)
PhoneInfoga, Sherlock, Holehe, SpiderFoot, Twint, GHunt, LinkFinder,
SecretFinder, ParamSpider, Arjun, FFUF, Nuclei Templates

---

## Important notes

- **Installer only** – this script downloads and installs tools. It does not run them.
  Once installed, you can launch the tools from the Start Menu, command line, or
  wherever they normally live.

- **No freezing** – the script has been thoroughly debugged. Menus respond instantly,
  and the detection loop never hangs.

- **Fallback methods** – if winget doesn’t find a package, the script will try
  Chocolatey. If Chocolatey isn’t installed, it will attempt a direct download.
  Only if all methods fail will it report the installation as unsuccessful.

- **Python version** – stick to 3.11 or 3.12. Some older tools (like dnsrecon or
  theHarvester) may not work on Python 3.13+.

---

## What’s new in this release?

- First public Windows release.
- Complete rewrite of the original fsociety concept in Python 3.
- Added 12 extra tools curated by azooz64 (category 14).
- Robust multi‑method installer with automatic fallbacks.
- Instant tool detection after every install.
- Improved error handling – the terminal never disappears unexpectedly.

---

## Upcoming

- Automatic updates for existing installations
- Configurable tool lists (user‑defined favourites)
- Linux & macOS releases already available in the main repository

---

## Credits & License

Developed and maintained by azooz64.
Licensed under the MIT License – free to use, modify, and distribute.

---

Happy hacking!
— azooz64
