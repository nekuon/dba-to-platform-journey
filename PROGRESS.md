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
