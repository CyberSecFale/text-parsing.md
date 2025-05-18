# text-parsing.md

# Parsing a Text File in a Security Scenario

I used Python to parse a log file and extract IP addresses involved in a simulated attack scenario. The script scanned the log for entries marked "ATTACK" and extracted the associated IP addresses for further investigation.

```python
with open('log.txt', 'r') as file:
    for line in file:
        if 'ATTACK' in line:
            ip = line.split()[3]
            print(f"Suspicious IP: {ip}")

Outcome: Identified malicious IPs, which were then blocked to prevent further attacks.

Tools Used: Python, text editor for log analysis.
