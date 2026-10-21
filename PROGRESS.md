## Day 3 (2026-10-20)
**Week of Oct 19:** 11 / 25 so far (Day 2: 6.5 hrs, Day 3: 4.5 hrs)
- **Hours studied today:** 4.5 hrs
- **What I learned:** On a folder, x means permission to enter it with cd. After chown, labuser became the owner of note.txt and I became one of the "others," who only have read permission, so I couldn't write to it. 644 means -rw-r--r--, 755 means -rwxr-xr-x, and 640 means -rw-r-----.
- **Commands I used:** `id`, `groups`, `chmod`, `chown`, `useradd`, `passwd`, `usermod`, `groupadd`, `userdel`, `groupdel`, `sudo`
- **What broke / confused me:** I made typos: tourch instead of touch, chmond instead of chmod, and lauser instead of labuser. I also ran chmod 640 plan.txt from the day3 folder when the file was in team-docs/.
- **How I fixed it:** For the typos, the message said "command not found" (or "user does not exist"), which meant the name was wrong, so I retyped it. For plan.txt, the message said "No such file or directory," which meant the path was wrong, so I used team-docs/plan.txt.
- **Quiz scores:** 6 / 7. I first answered only two questions (1.25 points), then finished the quiz and improved two answers after feedback.
- **Biggest lesson:** Use Tab to complete names and re-read each command before pressing Enter.

## Next up

Day 4: text processing (grep, pipes, find, nano). Day 5: weekly test. Fix dnf before Week 2.
