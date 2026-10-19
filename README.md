# secure_scan_pro
A professional, GUI-based network scanner built on top of Nmap designed for security professionals and ethical hackers.

✨ Features

🎯 Multi-target scanning — scan comma-separated IPs, hostnames, or CIDR ranges simultaneously

🔄 4 Scan Modes:

Quick Scan — Top 100 ports with service detection

Aggressive (-A) — Full OS detection, version detection, scripts, traceroute

Top 1000 Ports — Broad coverage with service version detection

UDP Scan (-sU) — Top 100 UDP ports

📋 Real-time log output — timestamped live scan results in the GUI

💾 JSON Report Export — auto-named reports with full scan data

⏹️ Stop mid-scan — interrupt multi-target queue any time

⌨️ Keyboard shortcuts — Esc to stop, Ctrl+S to export

🌙 Dark mode UI — built with CustomTkinter

🛠️ Requirements

System Requirements

Nmap must be installed and available in your system PATH

Windows: Download Nmap (installer adds to PATH automatically)

Linux: sudo apt install nmap or sudo yum install nmap

macOS: brew install nmap

Python Requirements

Python 3.8 or higher

Install Python dependencies:
pip install -r requirements.txt

🚀 Installation & Usage
Option 1: Run from Source
# 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/SecureScanPro.git
cd SecureScanPro

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the app
python secure_scan_pro.py

Option 2: Windows Executable (Build it yourself)
pip install pyinstaller
pyinstaller SecureScanPro.spec
The executable will be in the dist/ folder.

Note: The .spec file bundles nmap.exe from C:\Program Files (x86)\Nmap\nmap.exe.
Update the path in SecureScanPro.spec if your Nmap installation is in a different location.

📁 Project Structure
SecureScanPro/
├── secure_scan_pro.py          # Main application source
├── SecureScanPro.spec          # PyInstaller build spec
├── requirements.txt            # Python dependencies
├── assets/
│   └── icon.ico                # Application icon
├── reports_sample/
│   └── secure_scan_pro_report_*.json   # Example report output
├── .github/
│   └── ISSUE_TEMPLATE/
│       ├── bug_report.md
│       └── feature_request.md
├── .gitignore
├── LICENSE
└── README.md

📄 Report Format
Reports are exported as JSON files named secure_scan_pro_report_YYYYMMDD_HHMMSS.json.

Each entry contains:
{
  "target": "scanme.nmap.org",
  "mode": "Aggressive (-A)",
  "output": "...(full nmap output)...",
  "time": "2026-04-25 16:49:32.718513"
}

⚙️ Building from Source (Windows)
Make sure Nmap is installed at C:\Program Files (x86)\Nmap\
(or update the path in SecureScanPro.spec)
Install PyInstaller: pip install pyinstaller
Build:
pyinstaller SecureScanPro.spec
Find your executable at dist/SecureScanPro.exe

⚠️ Legal Disclaimer
This tool is intended for authorized security testing and educational purposes only.

Only scan systems and networks you own or have explicit written permission to test.
Unauthorized port scanning may be illegal in your jurisdiction.
The author is not responsible for any misuse of this tool.
Always obtain proper authorization before scanning any network or system.

🤝 Contributing
Contributions are welcome! Please:

Fork the repository
Create a feature branch (git checkout -b feature/my-feature)
Commit your changes (git commit -m 'Add my feature')
Push to the branch (git push origin feature/my-feature)
Open a Pull Request
See .github/ISSUE_TEMPLATE/ for bug reports and feature requests.

