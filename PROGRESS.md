## Week 2, Day 1: Processes (Thu 5 Nov 2026)

Hours spent: 3 hrs

What I did: I learn the difference between a program and a process. For process i used 'sleep', 'ps aux'.'top', 'free -h'. I created a txt file (answers.txt) and printed content

What worked: I was able to run sleep program after a desired time like 'sleep 600' and also run it in background 'sleep 600 &'. I was able to print the PID. I was able to kill the process

What was hard or went wrong: For getting the '&' after 'sleep' which froze the terminal(i should have used ctrl+C. Miss spelling file name (eventually renamed). Typing nano twice.I learnt only a user can delete its own command if i must use another user it must be a super user

Commands I now know: 'sleep 900 &', 'ps aux | grep chonyd', 'pgrep -u postgres postgres', 'kill PID' 'fg/bg', 'kill -9', 'pkill mysleep','jobs','uptime', Ctrl+C and Ctrl+Z.

Next: Week 2, Day 2 (services)

## Week 2, Day 2: Services 

Hours spent:4.5 hrs

What I did: I worked with systemd. I explored service running (how to stop, start, restart). I discover how to tell if its enabled and diabled. I discovered to execute code as Administrator, sudo has to be used first (also because it in the root). Also how to create a unit file. After making any change to unit file daemon-reload (sudo systemctl daemon-reload) must be ran. 

What worked: Execution of unit file.

What was hard or went wrong: Typo error. case sensitivity for ExecStart and WantBy. Forgetting to run daemon-reload after changing a unit file 

Commands I now know: 'systemctl status chronyd' 'systemctl is-active chronyd' 'systemctl is-active chronyd''systemctl is-enabled chronyd' 'sudo systemctl start chronyd''sudo systemctl stop chronyd''sudo systemctl restart chronyd''reload''systemctl is-enabled chronyd' 'ps  -p 1'' sudo systemctl daemon-reload' systemctl is-active chronyd = print active or inactive'

Next: Week 2, Day 3 (logs)
