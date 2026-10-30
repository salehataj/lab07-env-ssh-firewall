# Lab 07 – Challenge Tasks

## 1. Environment Variable Auditing

I used the `printenv` command to display environment variables available in the Ubuntu system. I filtered the PATH, LANG, and PWD variables using the `grep` command. PATH stores directories where the system searches for executable commands, LANG defines the language and locale settings, and PWD stores the current working directory.

## 2. Temporary Student Environment Variables

I created three temporary environment variables using the `export` command: STUDENT_NAME, STUDENT_ROLL_NUMBER, and STUDENT_SEMESTER. I displayed their values using the `echo` command. After logging out and reconnecting, these variables were no longer available because temporary environment variables do not persist after the session ends.

## 3. Permanent Student Environment Variables

To make the student variables permanent, I added their export commands at the end of the `~/.bashrc` file using Vim. I applied the changes using `source ~/.bashrc`. The variables then became available automatically in new interactive Bash sessions.

## 4. Blocking Incoming Ping Requests Using UFW

I created a backup of `/etc/ufw/before.rules` before making changes. I located the incoming ICMP echo-request rule and changed its target from ACCEPT to DROP. This instructed the firewall to drop incoming ping requests. I reloaded UFW to apply the updated firewall rules and tested the configuration.

## 5. Restoring the Original Firewall Rule

After testing, I changed the DROP target back to ACCEPT and reloaded UFW. This restored the original behavior and allowed incoming ping requests according to the firewall configuration.
