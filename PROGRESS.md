# PROGRESS LOG

## Phase 0: Foundations
**Current week/day:** Week 1, Day 2
**Hours studied this week:** 4 / 25

## Day 1 (2026-10-08)
- **What I learned:** Understanding the difference between the terminal, the shell and the kernel. Understanding how to run simple commands like pwd, ls, ls -al, and others
- **Commands I used:** pwd, ls, ls -l, ls -lh, ls -a, cd, cd .., cd ~, cd -, mkdir, mkdir -p, touch, man, whoami, free -h, df -h, nproc
- **What broke / confused me:** leaving off - after a command for example:ls l; instead of ls -l; forgetting the space in cd.., cd ..;cd../../../ instead of cd ../../../
- **How I fixed it:** "slowed down" to accomplish task writing ls -lh instead of ommiting -, ensuring there is space in cd ../../../ instead of cd../../../
- **Quiz score:** 7 / 8
- **Challenge completed?** yes
- **Snapshot taken?** yes (clean-start)
- **System:** Red Hat Enterprise Linux 9.4 in VirtualBox, 2 CPUs, 5.4 GiB RAM

## Day 2 (2026-10-19)
- **Hours studied today:** 6.5 hrs
- **What I learned:** I learnt moving folders and renaming them. With echo "line 1" > notes.txt, the > replaces everything in the file, but with echo "line 2" >> notes.txt, the >> adds to the end and keeps what was already there.
- **Commands I used:** `mv`, `cp -r`, `rm -i`, `rm -ri`, `rmdir`, `cat`, `head`, `tail`, `less`, `echo`, `rpm -q`, `dnf repolist`
- **What broke / confused me:** Created day2 in the wrong folder and moved it back with 'mv day2 ..'. Also dnf shows no repositories available through subscriptions.
- **How I fixed it:** I moved day2 up into week1 with mv day2 .. and used pwd to check where I was. I learned that rmdir only removes empty folders, so to remove a folder with contents I use rm -ri, which asks before deleting. For the clock issue I started troubleshooting with command 'date', then timedatectl. I entered 'sudo systemctl restart chronyd' then then 'sudo chronyc makestep', which failed with command not found because of a typo. I reran 'date'and 'timedatectl' and noticed clock was synchronized. dnf still lists only the install-disc repository, even after the clock fix, refresh, and trying to enable the repositories.
- **Quiz scores:** 3/7, then 3.5/7, then 6.25/7 after doing it hands-on
- **Biggest lesson:** Avoid typo errors. Spent too much time correcting them. Learnt to pace myself doing exercises.


## Day 3 (2026-10-20)
**Week of Oct 19:** 11 / 25 so far (Day 2: 6.5 hrs, Day 3: 4.5 hrs)
- **Hours studied today:** 4.5 hrs
- **What I learned:** On a folder, x means permission to enter it with cd. After chown, labuser became the owner of note.txt and I became one of the "others," who only have read permission, so I couldn't write to it. 644 means -rw-r--r--, 755 means -rwxr-xr-x, and 640 means -rw-r-----.
- **Commands I used:** `id`, `groups`, `chmod`, `chown`, `useradd`, `passwd`, `usermod`, `groupadd`, `userdel`, `groupdel`, `sudo`
- **What broke / confused me:** I made typos: tourch instead of touch, chmond instead of chmod, and lauser instead of labuser. I also ran chmod 640 plan.txt from the day3 folder when the file was in team-docs/.
- **How I fixed it:** For the typos, the message said "command not found" (or "user does not exist"), which meant the name was wrong, so I retyped it. For plan.txt, the message said "No such file or directory," which meant the path was wrong, so I used team-docs/plan.txt.
- **Quiz scores:** 6 / 7. I first answered only two questions (1.25 points), then finished the quiz and improved two answers after feedback.
- **Biggest lesson:** Use Tab to complete names and re-read each command before pressing Enter.


## Day 4 (2026-10-21)
- **Hours studied today:** 4 hrs
- **What I learned:** I learnt in this section pipe grep and nano. nano is a text edit software. pipe is used to input the output of a command. And grep is used to search for a specific text pattern inside a file or stream output
- **Commands I used:** `>`, `>>`, `2>`, `|`, `wc`, `sort`, `grep`, `find`, `nano`
- **What broke / confused me:** I forgot to attach the word "echo" eg echo hi >> same.txt .
- **How I fixed it:**  I had to correct myself in including the word echo
- **Quiz scores:** I had to take the quiz multiple times. I eventually scored 6.5/7. I should know by now how to be more specific answering questions
- **Biggest lesson:** I have to improve on my typos. The tab button will be of needed help.

Week 1 complete (Day 5 done)
- **Hours studied today:** 3 hrs
- **What I learned:** I learnt utilizing commands like grep, mkdir -p, mkdir -p project/{docs,scripts,logs,backup} to create project subfolders docs,scripts,logs and backup
- **Commands I used:** `mkdir -p`, `touch`, `echo`, `>>`, `grep`, `chmod`, `cp -r`, `find`, `wc -l`, `|`, `rm -ri`, `nano`
- **What broke / confused me:** typo, still errors like la instead of 'ls'
- **How I fixed it:** I adapted utilizing the tap in completing my typos.
- **Test scores:** first try 8.25 / 12, retake 10.25 / 12
- **Biggest lesson:** Change habits, using tab to complete text
## Week 1 summary (Days 1 to 5)

| Day | Topic | Hours | Score |
|---|---|---|---|
| 1 | Terminal, files and folders | 4 | 7 / 8 |
| 2 | Copy, move, delete, read files | 6.5 | 6.25 / 7 |
| 3 | Users and permissions | 4.5 | 6 / 7 |
| 4 | Redirection, pipes, grep, find, nano | 4 | 6.5 / 7 |
| 5 | Week 1 lab and test | | 10.25 / 12 |

- **Total hours for Week 1:** 22 hrs
- **Things I can now do:** bacis Linux comand
- **Things I still need to practice:** I need to accuse the tap for complete inputs
- **Open problem:** dnf shows only the install-disc repository. Next step: register the VM under my own Red Hat Developer account.


## Week 2, Day 1: Processes (Thu 5 Nov 2026)

Hours spent: 3 hrs

What I did: I learn the difference between a program and a process. For process i used 'sleep', 'ps aux'.'top', 'free -h'. I created a txt file (answers.txt) and printed content

What worked: I was able to run sleep program after a desired time like 'sleep 600' and also run it in background 'sleep 600 &'. I was able to print the PID. I was able to kill the process

What was hard or went wrong: For getting the '&' after 'sleep' which froze the terminal(i should have used ctrl+C. Miss spelling file name (eventually renamed). Typing nano twice.I learnt only a user can delete its own command if i must use another user it must be a super user

Commands I now know: 'sleep 900 &', 'ps aux | grep chonyd', 'pgrep -u postgres postgres', 'kill PID' 'fg/bg', 'kill -9', 'pkill mysleep','jobs','uptime', Ctrl+C and Ctrl+Z.

Next: Week 2, Day 2 (services)


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

## Week 2, Day 3: Logs (14 November 2026)

Hours spent: 4 hrs

What I did: I learnt how to lookup an collect logs both binary/memory and write plane-text format to dick for long term storage. Leant how to read them and interprit them.

What worked:
Calling systemd using 'sudo journalctl -n 20 --no-pager also verifying services logs such as 'sudo journalctl -u postgresql-16 --no-pager

What was hard or went wrong:
Typo errors. examples sudo jornalctl etc/systemd/..... forgetting the '/'

Commands I now know:
'ls /var/log''sudo tail -5 /var/log/messages''sudo journalctl -n 20 --no-pager''sudo journalctl -u chrony -n 15 --no-pager''sudo journalctl --since "10 minutes ago" --no-pager''sudo journalctl -p err -n 20 --no-pager''sudo journalctl -b -n 5 --no-pager''sudo journalctl --list-boot''... | grep chrony'... | wc -l''logger "TEXT"''clear'

Next: Week 2, Day 4 (packages)

## Week 2, Day 4: Packages (November 16, 2026)

**Hours spent:** 6 hr

### What I did
* Learned how to query the system using both `rpm` and `dnf` to inspect installed packages, configuration files, and transaction history.
* Diagnosed a broken local repository (`mnt_rhel-iso_`) by checking repo files, mount points, and block devices.

### What worked
* Successfully queried the RPM database for package counts, file ownership, package metadata, and recently installed software.
* Traced why `dnf` failed to download metadata by verifying that `/mnt/rhel-iso` was empty and `sr0` held the VirtualBox Guest Additions ISO instead.

### What was hard or went wrong
* Working with `dnf` repository queries and troubleshooting why `dnf repolist` succeeded while metadata checks failed due to an unmounted local ISO repo.

### Commands I now know
* `rpm -qa | wc -l` — Count all installed packages
* `rpm -qa | head -5` — View the first 5 installed packages
* `rpm -qa | grep -i WORD` — Search installed packages case-insensitively
* `rpm -q NAME` — Check if a specific package is installed
* `rpm -qi NAME` — Show detailed info for a package
* `rpm -ql NAME | head -15` — List the first 15 files owned by a package
* `rpm -qc NAME` — List configuration files for a package
* `rpm -qf /PATH` — Identify which package owns a specific file
* `rpm -qa --last | head -10` — Show the 10 most recently installed packages
* `rpm -V NAME` — Verify a package's files against the RPM database
* `sudo dnf --disablerepo="*" history` — View `dnf` transaction history without checking remote repos
* `sudo dnf repolist` — List enabled repositories
* `ls /etc/yum.repos.d/` — View repository configuration files
* `lsblk` — Check block devices and optical drive mounts
* `mount | grep rhel` — Check active RHEL filesystem mounts

**Next:** Week 2, Day 5 (Web server project)

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

## Week 3, Day 1: Networking basics (Nov 22 2026)

Hours spent:3 hrs

What I did:
I learnt how to find interface and address of networks, the route, list devices and status, how to ping (specific times) an address and examing everything listening on an adddres. Found out the template asked for: 127.0.0.1 means only this machine can connect, and * means any address can

What worked:
The general command worked like sudo ss -tulpn. Found out that PostgreSQL listens only locally

What was hard or went wrong:
Forgetting to include the - in command ip -br addr also skipping the number in the ping

Commands I now know:
hostname        the machine's name
hostnamectl     more detail: name, whether it is a VM, the OS
ip -br addr     the interfaces and their addresses, on one line each (-br = brief)
ip addr show enp0s3     the full detail for one interface. The name comes from the line before.
ip route        the routes. The line starting default names the gateway after via.
nmcli device status     NetworkManager's list of devices and their status
ping -c 3 ADDRESS       send 3 test packets, then stop (-c 3 = count). Without -c, it runs until Ctrl+C.
sudo ss -tulpn  everything listening: -t TCP, -u UDP, -l listening, -p the program, -n numbers, not names
sudo ss -tulpn | grep httpd     only the lines about httpd
curl -s http://localhost:8080   ask the server on port 8080 (:8080 after the name = that port)

Next: Week 3, Day 2 (names, ports and the firewall)

## Week 3, Day 2: Names, ports and the firewall (Nov 24 2026)

Hours spent: 7 hrs

What I did:

I cleaned my repo. Github was cleaned and committed to branch. Also i learnt how to reach and listen on a port. Checked my VM's active DNS servers in /etc/resolv.conf and via nmcli, and tested name resolution with getent and ping. Looked up standard service-to-port mappings

What worked:

getent hosts redhat.com resolved redhat.com to 52.200.142.250 and 34.235.198.240, proving DNS resolution works even when ICMP ping is blocked by Red Hat's servers. Using git log --stat clearly showed commits with many minus signs, leading straight to the 10 snapshots holding lost entries. Using git show HASH:PROGRESS.md recovered every missing day from Week 1 and Week 2 without changing or breaking my live files. Slicing entries with sed and appending with >> rebuilt a complete, chronological PROGRESS.md with 173 lines restored.

What was hard or went wrong:

I noted that omitting -a on sudo tee -a /etc/hosts would wipe out the entire hosts file; I learned to always back up system files first (cp /etc/hosts /etc/hosts.bak) and double-check append flags. Running git log inside a regular folder failed because the repository hadn't been cloned yet, I learned I must work inside the cloned repo folder.

Commands I now know:

Command | Plain words

cat /etc/resolv.conf     which DNS server the machine uses

nmcli device show enp0s3 | grep -i dns     the DNS servers NetworkManager gives that interface

getent hosts redhat.com     look up a name the way programs do (hosts file, then DNS)

getent ahosts localhost | head -3     all addresses for a name, in the order programs try them

grep "^hosts" /etc/nsswitch.conf     the lookup order

sudo cp /etc/hosts /etc/hosts.bak     make a backup copy

echo "127.0.0.1 myweb" | sudo tee -a /etc/hosts     add a line to the hosts file as root. -a is essential. Without it, tee replaces the whole file.

getent services http     the port number for a service name

sudo firewall-cmd --get-active-zones     the zones in use, and their interfaces

sudo firewall-cmd --list-all     everything the active zone allows

sudo firewall-cmd --list-    ports only the ports opened by number

sudo firewall-cmd --add-port=8080/tcp     open TCP port 8080 now only

sudo firewall-cmd --reload     apply the permanent settings, and drop the runtime-only ones

git status     where he is, and whether anything changed

git remote -v     the address of the remote

git --no-pager log --oneline     the commits, one per line, without the pager. The option goes before log, like dnf --disablerepo.

git --no-pager log --oneline -- PROGRESS.md     only the commits that touched that file (-- separates the options from the file name)

git --no-pager log --oneline --stat -- PROGRESS.md     the same, plus how many lines each commit added and removed

git pull     download new commits from GitHub and update his copy

git show 8c1ce66:PROGRESS.md     the file as it was in commit 8c1ce66

grep -nE "^(#+ |Day [0-9]|Week [0-9])" FILE       the heading lines of an entry file, with line numbers (-E lets | mean "or"). In the terminal he types the | as a plain |... see the note below.

sed -n '10,40p' FILE     print lines 10 to 40 add to the end of a file

Next: Week 3, Day 3 (storage basics)
