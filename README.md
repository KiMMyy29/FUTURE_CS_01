# FUTURE_CS_01
# Website Security Assessment Report

Overview
This project presents a cybersecurity vulnerability assessment conducted on the Wikipedia website using ethical and non-intrusive techniques.

The objective was to identify common security weaknesses, classify risks, and provide practical recommendations in a professional audit format.

Website Tested
- https://www.wikipedia.org/

Scope
- Public-facing pages only
- Passive analysis only
- No exploitation or harmful actions performed

Tools Used
- Nmap – Port and exposure analysis  
- OWASP ZAP (Passive Scan) – Automated vulnerability identification  
- Browser Developer Tools – HTTP header and configuration analysis  

Identified Vulnerabilities & Findings

5a. Potential Path Traversal (OWASP ZAP Passive Scan)
Risk Level: High  
OWASP ZAP flagged a potential path traversal vulnerability. This could allow unauthorized access to restricted files.
This was not confirmed due to scope limitations and may represent a false positive.

5b. Potential SQL Injection (OWASP ZAP Passive Scan)
Risk Level: High 
The scan identified patterns suggesting a possible SQL Injection vulnerability, which could allow database manipulation if exploited.
This finding is unverified and based only on automated analysis.

5c. Additional Observations from OWASP ZAP Passive Scan
Risk Level: Medium–Low  
Additional alerts were raised related to configuration and response handling, which may contribute to security weaknesses if not properly managed.

Information Disclosure via HTTP Headers  
Risk Level: Low  
The server exposes implementation details, which may assist attackers in identifying technologies in use.

Missing or Limited Security Headers  
Risk Level: Low  
Some recommended security headers are not fully implemented, reducing protection against certain client-side attacks.

Open Ports Exposure (Nmap Scan)  
Risk Level: Low  
The scan revealed open ports:
- Port 80 (HTTP)  
- Port 443 (HTTPS)  

While expected for a public website, open ports represent potential entry points and must be properly secured.

Risk Summary
- High Risk: 2 
- Medium Risk: 4  
- Low Risk: 3
- Informal: 1 

Recommendations
- Validate automated scan findings to rule out false positives  
- Minimize server information disclosure  
- Implement additional security headers  
- Maintain strict firewall and port management  
- Continuously monitor and update security configurations  

Report
The full vulnerability assessment report is included in this repository.

Disclaimer
This assessment was conducted strictly under ethical guidelines. No intrusive techniques or exploitation methods were used. Some findings are based on automated tools and may require further validation.
