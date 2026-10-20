# PROGRESS LOG

## Phase 0: Foundations
**Current week/day:** Week 1, Day 1 (Linux command line basic)
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
- **Hours studied today:** 4.5 hrs
- **What I learned:** I learnt moving folders and renaming them. With echo "line 1" > notes.txt, the > replaces everything in the file, but with echo "line 2" >> notes.txt, the >> adds to the end and keeps what was already there.
- **Commands I used:** `mv`, `cp -r`, `rm -i`, `rm -ri`, `rmdir`, `cat`, `head`, `tail`, `less`, `echo`, `rpm -q`, `dnf repolist`
- **What broke / confused me:** Created day2 in the wrong folder and moved it back with 'mv day2 ..'
- **How I fixed it:** I moved day2 up into week1 with mv day2 .. and used pwd to check where I was. I learned that rmdir only removes empty folders, so to remove a folder with contents I use rm -ri, which asks before deleting.
- **Quiz scores:** 3/7, then 3.5/7, then 6.25/7 after doing it hands-on
- **Biggest lesson:** Avoid typo errors. Spent too much time correcting them. Learnt to pace myself doing exercises.

- ## Next up
Red Hat registration check, then Day 3: users and permissions
