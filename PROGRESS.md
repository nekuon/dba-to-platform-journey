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
