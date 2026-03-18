# Fail2Ban SSH Security Lab

Hands-on project: Set up Fail2Ban on Ubuntu to protect SSH from brute-force attacks, simulated real attacks from Kali Linux, and added automated email alerts on bans.

## What I Did

1. Installed and configured Fail2Ban
2. Created custom SSH jail (3 failed attempts in 60s → 60s ban)
3. Fixed common issues: config syntax errors, duplicate jail files, ignoreip overriding bans, service startup failures
4. Tested with real brute-force simulation from separate Kali machine
5. Set up Postfix + Gmail relay for automated ban notifications (with whois + log excerpts)
6. Verified bans in real time via `fail2ban-client status` and logs

## Technologies Used

- Ubuntu (server)
- Fail2Ban
- OpenSSH (key-based auth + temporary password auth for testing)
- Postfix (send-only mail relay)
- Gmail SMTP (with app password)
- Kali Linux (attack simulation)
- iptables (underlying ban mechanism)
