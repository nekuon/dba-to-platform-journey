## Week 2 complete (Day 5 done)

Hours studied today: 6 hrs 
What I learned: How to deploy, inspect, and troubleshoot an Apache HTTP (`httpd`) web server by combining Week 2 skills—verifying package ownership (`rpm`), managing service state (`systemctl`), inspecting access logs (`/var/log/httpd/access_log`) and service journals (`journalctl -u httpd`), and checking firewall rules (`firewall-cmd`).
Commands I used: `systemctl status httpd`, `systemctl is-active httpd`, `sudo systemctl start httpd`, `rpm -q httpd`, `rpm -qf /usr/sbin/httpd`, `rpm -qf /usr/lib/systemd/system/httpd.service`, `sudo tail -n 5 /var/log/httpd/access_log`, `sudo journalctl -u httpd --since "10 minutes ago" --no-pager`, `sudo firewall-cmd --list-services`, `sed -n '1p' challenge.txt`
What broke / confused me:
1. Expected `sudo systemctl start httpd` to assign a new Main PID when `httpd` was already running from two days earlier.
2. Used `source challenge.txt`, which executed all 6 lines at once instead of one by one (`rpm` without `-q`, `journalctl` without `-u httpd`, and `firwall-cmd` misspelled).
How I fixed it:
1. Learned that `systemctl start` is idempotent—it does nothing if a service is already `active (running)` (only `restart` or `stop` + `start` creates a new PID).
2. Used `sed -n '1p' challenge.txt` (with `-n` for quiet mode) to inspect one line at a time, fixed the missing `-q`, `-u httpd`, and spelling of `firewall-cmd`, and re-verified each command.
Test scores: Day 5 Challenge: 11/12 (updated)
Biggest lesson: Double-check every flag and spelling before running commands, and remember that `systemctl start` leaves an already-running service untouched.

Week 2 summary (Days 1 to 5)

| Day | Topic | Hours | Score |
|---  |-------|-------|-------|
| 1 | Processes | 3 | 8.25/12 on retake 10.25/12 |
| 2 | Services | 4.5 | 5.25/7 |
| 3 | Logs | 4.5 | 4.1/7 |
| 4 | Packages | 6 | 5/6 |
| 5 | Web server project | 11/12| update after completion | 
Total hours for Week 2: 24 hours
Things I can now do:
- Inspect running processes and PIDs (`ps`, `pgrep`, `top`, `kill`)
- Start, stop, restart, enable, and check the status of `systemd` services
- Read service logs with `journalctl` and inspect files under `/var/log/`
- Query installed packages, file ownership, and package metadata with `rpm` and `dnf`
- Verify a working web server stack (`httpd` + logs + `firewalld`) and open multiple SSH sessions for side-by-side note-taking
Things I still need to practice:
- Writing exact command flags (`-q`, `-u`, `-n`) and spelling tool names (`firewall-cmd`) from memory without syntax slips
- Stepping through multi-line command files one line at a time (`sed -n 'Np'`) instead of running the whole file with `source`
Next up: Week 3
