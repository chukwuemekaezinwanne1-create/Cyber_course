# Fix lines 5 and 6, then CTRL+O, Enter, CTRL+X
git add README.mdgit add README.md git commit 
--amend -m "Day 1-6: Augustine Ezinwanne SOC 
Portfolio"git add README.md git commit 
--amend -m "Day 1-6: Augustine Ezinwanne SOC 
Portfolio" git commit -m "Fix contact details 
and GitHub link"
git push origin main
# Augustine's SOC Analyst Portfolio
cd ~/cyber_course**Goal:** Level 1 SOC 
Analyst at Flutterwave / Interswitch / 
Moniepoint **Tools Built:** 14 Python 
Security Scripts on Android Termux 
**GitHub:** github.com/Ezinwanne chkwuemeka 
augustine **Contact:** 
chukwuemekaezinwanne1@gmail.com 
**Location:** Nigeria | Available for 
remote/on-site nano README.md ---

## Tools Overview
python port_scanner.py| Day | Tool | SOC Use 
Case | Key Skills Demonstrated |
| --- | --- | --- | --- | 1 | ip_validator.py 
| | Input sanitization for firewalls | IP 
| validation, error handling | 2 | 
| password_checker.py | Enforce NIST password 
| policy | Strings, conditionals, security 
| standards | 3 | log_parser.py | Extract 
| IOCs from raw logs | File I/O, regex 
| thinking, data extraction | 4 | 
| ip_validator_v2.py | Detect private vs 
| public IPs | CIDR notation, network 
| segmentation | 5 | log_reader.py | Detect 
| brute force attacks | Log analysis, 
| alerting, TTP detection | 6 | 
| port_scanner.py | Find exposed services | 
| Sockets, TCP, risk assessment | 7-14 | 
| Coming soon | SIEM, Hashing, APIs | 
| Incident response workflow |

---

## Day 1: IP Validator
**SOC Problem:** Firewalls fail when given 
malformed IPs like `256.1.1.1`. Analysts must 
sanitize input first. **Code:** ```python 
print("=== SOC IP Validator ===") ip = 
input("Enter IP to validate: ") octets = 
ip.split('.')

if len(octets)!= 4: print("Invalid IP - must 
    have 4 octets")
else:
    valid = True
    for octet in octets:
        if not octet.isdigit() or not 0 <= int(octet) <= 255:
            valid = False
            break
    if valid:
        print(f"Valid IP: {ip}")
    else:
        print("Invalid IP - octet out of range")
