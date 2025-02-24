iREM-FW (Incremental Ransomware Emulation Framework)

Overview

iREM-FW (Incremental Ransomware Emulation Framework) is a modular and incremental framework designed for security professionals, red teamers, and SOC analysts to simulate ransomware behaviors in controlled environments. It provides a structured approach to testing endpoint detection and response (EDR), security information and event management (SIEM) alerts, and defensive controls against ransomware-like activity.

This framework was initially conceptualized and briefly covered in my ShmooCon 2025 FireTalk, where I discussed using humor and creative methodologies to stress-test security tools. iREM-FW extends those principles into a structured toolset for controlled ransomware emulation.

Key Features

Incremental Execution – Allows for staged and controlled execution of ransomware-like activities, making it ideal for security research and blue team validation.

AES-256 Encryption Simulation – Emulates ransomware encryption using AES-256 while ensuring reversibility for testing purposes.

Lateral Movement & C2 Emulation – Options for testing beaconing and command-and-control behaviors.

Customizable Payloads – Easily modify or create new scripts to match evolving threats.

SIEM/XDR Testing – Designed to trigger specific detections in modern security stacks, including Splunk, SentinelOne, and Cisco ETD.

Obfuscation & Evasion Techniques – Includes options for encoding, PowerShell execution, and process injection testing.

Safe Execution Mode – Ensures no actual harm to files in testing environments by using dummy data.

Installation

Prerequisites

Python 3.x (Recommended for script execution and encryption functions)

PowerShell 5.1+ (Required for Windows-based execution tests)

Virtualized Test Environment (VMware/VirtualBox/AWS/Isolated Lab recommended)

Clone Repository

 git clone https://github.com/yourusername/iREM-FW.git
 cd iREM-FW

Install Dependencies

 pip install -r requirements.txt

Usage

Running Incremental Ransomware Emulation

Basic Execution:

 python iREM.py --encrypt --test-mode

Simulated File Encryption:

 python iREM.py --encrypt --path /test-folder --key EmulationKey256SecretNotReally!

Beaconing Emulation (SliverC2/Havoc Integration Planned):

 python iREM.py --c2-test --ip 192.168.1.100

Testing & Deployment

This framework is designed to be used in controlled environments only. Do not deploy in production networks unless explicitly authorized by leadership and security operations.

Recommended Testing Setups:

Isolated VM Environment: Ideal for endpoint testing.

SIEM/XDR Monitoring: Validate detections and response workflows.

AWS Lab: Safe for large-scale behavioral analysis.

Roadmap

✅ Phase 1: Core AES-256 encryption emulation with controlled execution.✅ Phase 2: Base64-encoded execution & process injection tests.🔄 Phase 3: C2 beaconing emulation (Sliver/Havoc integration).🔄 Phase 4: Advanced obfuscation & evasion techniques.🔄 Phase 5: Community-driven enhancements & integration with real-world threat intelligence.

Legal & Ethical Disclaimer

This tool is intended for educational and security research purposes only. Unauthorized use of ransomware emulation tools on production systems, personal devices, or unauthorized networks is strictly prohibited. Users are responsible for ensuring they have the proper authorization before deploying or testing this framework.

Initial setup of repo 2/24/25 
