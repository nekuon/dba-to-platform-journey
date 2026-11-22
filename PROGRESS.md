## Week 1 complete (Day 5 done)

Hours studied today: 3 hrs
What I learned: I learnt utilizing commands like grep, mkdir -p, mkdir -p project/{docs,scripts,logs,backup} to create project subfolders docs, scripts, logs and backup
Commands I used: `mkdir -p`, `touch`, `echo`, `>>`, `grep`, `chmod`, `cp -r`, `find`, `wc -l`, `|`, `rm -ri`, `nano`
What broke / confused me: typo, still errors like `la` instead of `ls`
How I fixed it: I adapted utilizing the Tab key in completing my typos.
Test scores: first try 8.25 / 12, retake 10.25 / 12
Biggest lesson: Change habits, using Tab to complete text

Week 1 summary (Days 1 to 5)

| Day | Topic | Hours | Score |
|---|---|---|---|
| 1 | Terminal, files and folders | 4 | 7 / 8 |
| 2 | Copy, move, delete, read files | 6.5 | 6.25 / 7 |
| 3 | Users and permissions | 4.5 | 6 / 7 |
| 4 | Redirection, pipes, grep, find, nano | 4 | 6.5 / 7 |
| 5 | Week 1 lab and test | 3 | 10.25 / 12 |

Total hours for Week 1: 22 hrs
Things I can now do: basic Linux commands
Things I still need to practice: I need to use the Tab key to complete inputs
Open problem: dnf shows only the install-disc repository. Next step: register the VM under my own Red Hat Developer account.
Next up: Fix dnf, then Week 2: processes, packages, services and logs.

## Week 3, Day 1: Networking basics (Nov 22 2026)

Hours spent:3 hrs 

What I did:
I learnt how to find interface and address of networks, the route, list devices and status, how to ping (specific times) an address and examing everything listening on an adddres. Found out the template asked for: 127.0.0.1 means only this machine can connect, and * means any address can

What worked:
The general command worked like sudo ss -tulpn. Found out that PostgreSQL listens only locally

What was hard or went wrong:
Forgetting to include the - in command ip -br addr also skipping the number in the ping 

Commands I now know:
hostname	the machine's name
hostnamectl	more detail: name, whether it is a VM, the OS
ip -br addr	the interfaces and their addresses, on one line each (-br = brief)
ip addr show enp0s3	the full detail for one interface. The name comes from the line before.
ip route	the routes. The line starting default names the gateway after via.
nmcli device status	NetworkManager's list of devices and their status
ping -c 3 ADDRESS	send 3 test packets, then stop (-c 3 = count). Without -c, it runs until Ctrl+C.
sudo ss -tulpn	everything listening: -t TCP, -u UDP, -l listening, -p the program, -n numbers, not names
sudo ss -tulpn | grep httpd	only the lines about httpd
curl -s http://localhost:8080	ask the server on port 8080 (:8080 after the name = that port)

Next: Week 3, Day 2 (names, ports and the firewall)
