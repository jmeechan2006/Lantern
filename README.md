<p align="center">
  <img src="assets/lantern-logo.png" alt="Lantern logo" width="220">
</p>

# Lantern

A honeypot threat-intelligence project.

- **Pitcher** lures in and records real-world SSH attacks using a Cowrie honeypot on a cloud server.
- **Dashboard** shows where attacks come from, what they try, and what their goal is.

Work in progress.
Lantern's Dashboard currently runs on sample data.

## Data and privacy

Lantern does not publish attacker IP addresses. Many IP's that will attack a honeypot belong to innocent people whose devices, such as home routers, cameras, old servers, have been hijacked into a botnet without their knowledge.

- All public data is at a **country level**.
- Raw logs that contain IPs stay private on the honeypot server, and are deleted once the project is finished.
- Attack locations show where traffic came from, this is not always where the attackers are. Bots usually route traffic through hijacked devices, VPNs, and rented cloud servers.


## How the numbers are counted

- **Attack** : an attack is one session where a bot has made atleast one login attempt.
- **Login attempt** : every individual username and password guess.
- **Commands**: the number of sessions that ran each command.

## Planned features

- **City-level heatmap with k-anonymity**: shows attacks by city, but only where at least 5 unique attackers share a location. Any attacks from cities under 5 attackers will be rolled-up to the country instead so no individual can be identified.