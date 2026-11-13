## Week 2, Day 2: Services (November 12, 2026)

Hours spent: 4.5 hrs

What I did: I worked with systemd (PID 1), the service manager that controls all system services. I explored how to check, stop, start, and restart services like chronyd, and checked PostgreSQL (postgresql-16) and its 7 processes (1 parent and 6 workers). I discovered how to check if a service is enabled or disabled, and why sudo is required to manage services (because systemd runs as root, making service control an administrator job). I also wrote a custom unit file (mysleep.service) and learned to run sudo systemctl daemon-reload after every edit.

What worked: Writing and running my custom mysleep.service unit file, testing Restart=always after kill -9, and scripting my challenge commands cleanly.

What was hard or went wrong: Typo and case-sensitivity errors in the unit file (ExecStart and WantedBy), forgetting to run daemon-reload after editing a unit file, swapping stop and start order, running plain nano without sudo so it could not save in /etc/systemd/system/, and typing postgres instead of postgresql-16.

Commands I now know:
- `ps -p 1` = show PID 1 (systemd)
- `systemctl status chronyd` = show full status, Loaded state, Active state, and Main PID
- `systemctl is-active chronyd` = print active or inactive
- `systemctl is-enabled chronyd` = print enabled or disabled
- `sudo systemctl start chronyd` = start a stopped service now
- `sudo systemctl stop chronyd` = stop a running service now
- `sudo systemctl restart chronyd` = stop and immediately start a service with a new PID
- `sudo systemctl enable chronyd` = set a service to start automatically at boot
- `sudo systemctl disable mysleep` = stop a service from starting automatically at boot
- `sudo systemctl daemon-reload` = reload systemd after creating or editing a unit file
- `which sleep` = find the exact full path of the sleep binary (/usr/bin/sleep)
- `pgrep chronyd` = print the running PID(s) of chronyd

Next: Week 2, Day 3 (logs)
