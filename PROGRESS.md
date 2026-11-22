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
