🔍 Lab Write-up: Attacking a MySQL Database (Cisco CyberOps)
This repository documents my completion of the "Lab - Attacking a MySQL Database", part of the Cisco CyberOps curriculum. The lab provides hands-on experience analyzing a SQL injection attack captured in a PCAP file using Wireshark.

🧪 Lab Overview
The lab simulates a real-world SQL injection attack against a MySQL database. I analyzed the captured network traffic to trace the attack sequence and understand how an attacker extracts system and table information through malicious queries.

🧠 Skills Demonstrated
Analyzing MySQL traffic in Wireshark

Identifying SQL injection patterns

Understanding how attackers enumerate databases

Tracking sensitive data exfiltration from a MySQL server

Applying network forensics to real-world security scenarios

📋 Lab Walkthrough
🔹 Part 1: Open Wireshark and Load the PCAP
Loaded the PCAP file into Wireshark.

Applied filters to narrow down to SQL-related traffic (TCP port 3306).

Filter used:

wireshark
Copy
Edit
tcp.port == 3306
🔹 Part 2: View the SQL Injection Attack
Detected injection payloads such as:

vbnet
Copy
Edit
' OR 1=1 -- 
which are used to bypass login controls.

🔹 Part 3: Continued Injection Attempts
Observed the attacker issuing multiple queries to gather database insights and confirm successful injection.

🔹 Part 4: Extracting System Information
The attacker used:

scss
Copy
Edit
SELECT @@version;
SELECT user();
to extract system version and current user account details.

🔹 Part 5: Table Enumeration
Used:

pgsql
Copy
Edit
SELECT table_name FROM information_schema.tables;
to list available tables within the target database.

🔹 Part 6: Attack Conclusion
Final queries dumped data from sensitive tables, such as user credentials and emails.

📂 Tools Used
Wireshark

Cisco-provided PCAP file (simulated, non-malicious)

⚠️ Disclaimer
This lab was performed in a controlled educational environment. All actions and findings are intended strictly for cybersecurity training and awareness purposes.

