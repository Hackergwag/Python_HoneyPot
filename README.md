<h1>Python HoneyPot</h1>

<h2>Description</h2>
This project is a lightweight Python honeypot that listens on TCP port 2222, mimics an SSH service banner, and records all incoming connection attempts. Its purpose is to attract, log, and study real-world attackers who perform network scans or attempt unauthorized access, providing valuable insights into potential threats targeting servers and client systems.

The project highlights:

Built in Python – lightweight and easy to deploy.

Listens on TCP port 2222 to simulate an SSH service.

Emulates an SSH banner to attract attackers.

📜Logs connection attempts with timestamps and client details.

🕵🏽 Detects scans and intrusion attempts in real time.

Multi-threaded handling to manage multiple connections simultaneously.

🛠 Simple setup – no complex dependencies required.

Useful for learning & research about attacker behavior and network security.

This honeypot project showcases my SOC Analyst skills in threat detection and monitoring by logging real-time attacker activity, while also reflecting my Cybersecurity Engineering ability to design and build a Python-based defensive tool from scratch.
<br />

<h2>Languages and Utilities Used</h2>

- <b>Kali</b>
- <b>Python3</b>
- <b>cyberops</b>

<h2>Environments Used </h2>

- <b>Windows 10</b>

<h2>Program walk-through:</h2>

<p align="center">
python_honeypot_script: <br/>
<img src="https://imgur.com/Zr5j9Yr.png="Python_Hpneypot"/>
<br />
<br />
I wrote this script to run a lightweight Python honeypot that listens on 0.0.0.0:2222, emulates an SSH banner, handles connections concurrently with threads, and logs timestamps, client IPs and payloads for SOC monitoring and attacker analysis.<br />
<br />
Starting the HoneyPot:<br />
<br />
<img src="https://imgur.com/MLhmpb0.png" height="80%" width="80%" alt="Python_Hpneypot"/>
<br />
<br />
I started the honeypot, which is listening on TCP port 2222, and it displays a fake SSH banner while logging all connection attempts and any data sent by attackers.<br />
<br />
Attacking Attempt:<br/>
<img src="https://imgur.com/a87R2o0.png" height="80%" width="80%" alt="Python_Hpneypot"/>
<br />
<br />
This reflects the attack attempt made by the threat actor, shown here as a Telnet connection to the honeypot..<br />
<br />
<p align="center">
Attacking Self Attempt:<br/>
<img src="https://imgur.com/x3Fh2Gr.png" height="80%" width="80%" alt="Python_Hpneypot"/>
<br />
<br />
I tested my honeypot by acting as an attacker from another terminal, using Netcat to connect to the honeypot and send a message, which allowed me to demonstrate that the honeypot successfully captured the connection, recorded the data sent, and logged the entire interaction for analysis.<br />
<br />
<p align="center">
HoneyPot Alert Logs:  <br/>
<img src="https://imgur.com/31D4uvL.png" height="80%" width="80%" alt="Python_Hpneypot"/>
<br />
<br />
The honeypot alert logs capture and record all attacker activity, including Nmap scans from reconnaissance, Telnet connections from the attacking system, and Netcat interactions from my testing system, providing detailed data on the type and content of payloads sent, which allows SOC operations to analyze attacker motives, detect attempts to execute reverse shells, and understand potential strategies for creating persistent backdoors or other malicious actions.<br />
<br />
Saved Copy of the Logs From the Python Script:  <br/>
<img src="https://imgur.com/7Kv3xZK.png" height="80%" width="80%" alt="Python_Hpneypot"/>
<br />
<br />
The Python script was designed to generate and save a log copy at /home/kali/honeypot.log, enabling the SOC team to conduct further investigations, block suspicious IPs, and integrate the alert logs with SIEM tools like Splunk for deeper analysis and incident response.<br />
<br />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
