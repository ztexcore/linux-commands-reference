# Linux Commands Reference

> A comprehensive reference of Linux commands organized by category.
> **547 commands** across **18 categories**.

## Download
📄 [Download PDF Version](linux_commands_reference.pdf)

---

## Table of Contents

1. [File & Directory Management](#file-directory-management) — *20 commands*
2. [File Viewing & Editing](#file-viewing-editing) — *38 commands*
3. [File Permissions & Ownership](#file-permissions-ownership) — *8 commands*
4. [File Compression & Archiving](#file-compression-archiving) — *15 commands*
5. [Process Management](#process-management) — *28 commands*
6. [System Information](#system-information) — *24 commands*
7. [Disk & Filesystem](#disk-filesystem) — *31 commands*
8. [Networking](#networking) — *49 commands*
9. [User & Group Management](#user-group-management) — *22 commands*
10. [Package Management](#package-management) — *22 commands*
11. [Shell & Scripting](#shell-scripting) — *40 commands*
12. [Text Processing](#text-processing) — *18 commands*
13. [System Monitoring & Performance](#system-monitoring-performance) — *26 commands*
14. [Boot & Init](#boot-init) — *18 commands*
15. [Security & Cryptography](#security-cryptography) — *29 commands*
16. [Development & Debugging](#development-debugging) — *44 commands*
17. [Help & Documentation](#help-documentation) — *13 commands*
18. [Miscellaneous Utilities](#miscellaneous-utilities) — *102 commands*

---

## File & Directory Management

| Command | Description |
|---------|-------------|
| `ls` | List directory contents. Shows files and subdirectories in the current or specified directory. |
| `cd` | Change directory. Moves the shell's working directory to the specified path. |
| `pwd` | Print working directory. Displays the full absolute path of the current directory. |
| `mkdir` | Make directory. Creates one or more new directories at the specified path(s). |
| `rmdir` | Remove directory. Deletes empty directories; fails if the directory contains files. |
| `rm` | Remove files or directories. Permanently deletes files; use -r to remove directories recursively. |
| `cp` | Copy files or directories. Duplicates source to destination; use -r for directories. |
| `mv` | Move or rename files and directories. Relocates or renames a file/directory. |
| `touch` | Create an empty file or update the access/modification timestamps of an existing file. |
| `find` | Search for files in a directory hierarchy based on name, type, size, permissions, and more. |
| `locate` | Find files by name using a pre-built database index. Much faster than find for simple lookups. |
| `tree` | Display directory contents in a tree-like format, showing the hierarchy visually. |
| `ln` | Create hard or symbolic (soft) links between files. -s creates a symbolic link. |
| `realpath` | Print the resolved absolute path of a file, following all symlinks. |
| `stat` | Display detailed metadata about a file or filesystem: size, permissions, timestamps, inode. |
| `file` | Determine the type of a file by examining its content rather than its extension. |
| `basename` | Strip directory and optionally suffix from a file path, returning just the filename. |
| `dirname` | Return the directory component of a file path, stripping the filename. |
| `rename` | Rename multiple files at once using Perl-style regular expressions. |
| `shred` | Securely delete a file by overwriting its contents multiple times before removal. |

---

## File Viewing & Editing

| Command | Description |
|---------|-------------|
| `cat` | Concatenate and display file contents. Also used to combine multiple files into one. |
| `less` | View file contents one screenful at a time with backward/forward navigation. |
| `more` | View file contents page by page; unlike less, it only allows forward navigation. |
| `head` | Display the first N lines of a file (default 10). Useful for previewing large files. |
| `tail` | Display the last N lines of a file. -f follows a file live as it grows (e.g., logs). |
| `nano` | Simple, beginner-friendly terminal text editor with on-screen keybinding hints. |
| `vim` | Powerful modal text editor with extensive customization, macros, and plugin support. |
| `vi` | Original visual text editor; vi-compatible subset available on virtually all Unix systems. |
| `emacs` | Extensible, self-documenting text editor with built-in Lisp interpreter and vast ecosystem. |
| `gedit` | GNOME graphical text editor for desktop environments. |
| `diff` | Compare two files line by line and show the differences between them. |
| `patch` | Apply a diff (patch) file to update a file or source tree to a newer version. |
| `wc` | Word count: count lines, words, and bytes/characters in a file or standard input. |
| `sort` | Sort lines of text in a file or from stdin alphabetically, numerically, or by field. |
| `uniq` | Filter adjacent duplicate lines from sorted input; also counts or only shows duplicates. |
| `cut` | Extract specific columns or fields from each line of a file, delimited by a character. |
| `paste` | Merge corresponding lines from multiple files side by side, separated by a delimiter. |
| `join` | Join lines from two sorted files on a common field, similar to a database join. |
| `tr` | Translate, squeeze, or delete characters from standard input. E.g., convert case. |
| `sed` | Stream editor: perform text transformations (substitutions, deletions, insertions) on files. |
| `awk` | Powerful text-processing language that operates on records and fields within files. |
| `grep` | Search for lines matching a pattern (regex) in files or standard input. |
| `egrep` | Extended grep: same as grep -E, supports extended regular expressions. |
| `fgrep` | Fixed-string grep: same as grep -F, treats the pattern as a literal string (faster). |
| `strings` | Extract printable strings from binary files, useful for basic binary analysis. |
| `od` | Octal dump: display file contents in octal, hex, decimal, or ASCII representations. |
| `xxd` | Create a hex dump of a file or convert a hex dump back to binary. |
| `nl` | Number the lines of a file and write to standard output. |
| `fold` | Wrap lines in a file to fit a specified width. |
| `expand` | Convert tab characters in a file to the equivalent number of spaces. |
| `unexpand` | Convert leading spaces back to tab characters in a file. |
| `col` | Filter reverse line feeds and other special characters from terminal output. |
| `colrm` | Remove specific columns from each line of a text file. |
| `column` | Format input into aligned columns; useful for making tabular data readable. |
| `fmt` | Simple text formatter that fills and joins lines to a specified width. |
| `pr` | Paginate or columnate files for printing, adding headers and page numbers. |
| `tac` | Reverse cat: display file contents in reverse line order (last line first). |
| `rev` | Reverse the characters on each line of a file or standard input. |

---

## File Permissions & Ownership

| Command | Description |
|---------|-------------|
| `chmod` | Change file mode (permissions): read, write, execute for owner, group, and others. |
| `chown` | Change the owner and/or group of a file or directory. |
| `chgrp` | Change only the group ownership of a file or directory. |
| `umask` | Set the default permission mask applied when new files or directories are created. |
| `getfacl` | Get file access control lists (ACLs), showing extended permission settings. |
| `setfacl` | Set file access control lists, allowing fine-grained permissions for specific users/groups. |
| `lsattr` | List file attributes on an ext2/ext3/ext4 filesystem (immutable, append-only, etc.). |
| `chattr` | Change special filesystem attributes on a file (e.g., make a file immutable). |

---

## File Compression & Archiving

| Command | Description |
|---------|-------------|
| `tar` | Tape archive: bundle files into a single archive (.tar). Add -z/-j for compression. |
| `gzip` | Compress files using the gzip algorithm (.gz). Use gunzip to decompress. |
| `gunzip` | Decompress files compressed with gzip. |
| `bzip2` | Compress files using the bzip2 algorithm (.bz2), generally better compression than gzip. |
| `bunzip2` | Decompress files compressed with bzip2. |
| `xz` | Compress files using the LZMA/xz algorithm (.xz), offering very high compression ratios. |
| `unxz` | Decompress files compressed with xz. |
| `zip` | Package and compress files into a .zip archive compatible with Windows and other OSes. |
| `unzip` | Extract files from a .zip archive. |
| `7z` | Work with 7-Zip archives (.7z) and many other formats with high compression. |
| `zcat` | Display the contents of a gzip-compressed file without decompressing it to disk. |
| `zless` | View a gzip-compressed file with less without fully decompressing it. |
| `bzcat` | Display the contents of a bzip2-compressed file without decompressing to disk. |
| `rar` | Create RAR archives (proprietary format, requires non-free package). |
| `unrar` | Extract files from RAR archives. |

---

## Process Management

| Command | Description |
|---------|-------------|
| `ps` | Report a snapshot of current processes. ps aux shows all processes with details. |
| `top` | Interactive real-time process viewer showing CPU, memory usage, and system stats. |
| `htop` | Enhanced, colorful, interactive process viewer with mouse support (install separately). |
| `kill` | Send a signal to a process by PID. Default signal is SIGTERM (15) to request termination. |
| `killall` | Kill all processes matching a name. More convenient than finding individual PIDs. |
| `pkill` | Signal processes based on name or other attributes (regex support). |
| `pgrep` | Find the PIDs of running processes by name or attributes. |
| `nice` | Start a process with a modified scheduling priority (niceness from -20 to 19). |
| `renice` | Change the scheduling priority of an already-running process. |
| `nohup` | Run a command immune to hangup signals; keeps it running after you log out. |
| `bg` | Resume a suspended job in the background. |
| `fg` | Bring a background or suspended job to the foreground. |
| `jobs` | List active jobs (background/stopped processes) in the current shell session. |
| `wait` | Wait for a background process or job to complete before continuing. |
| `sleep` | Pause execution for a specified number of seconds (or minutes/hours/days). |
| `timeout` | Run a command with a time limit; kills it if it runs too long. |
| `watch` | Repeatedly execute a command at a fixed interval and display the output. |
| `at` | Schedule a command to run once at a specific time in the future. |
| `cron` | Daemon that runs scheduled tasks (cron jobs) defined in a crontab file. |
| `crontab` | Edit, list, or remove the cron job schedule for the current user. |
| `systemctl` | Control the systemd system and service manager: start, stop, enable, disable services. |
| `service` | Start, stop, restart, or check the status of a SysV init or systemd service. |
| `journalctl` | Query and display logs from the systemd journal. |
| `strace` | Trace system calls and signals made by a process; invaluable for debugging. |
| `ltrace` | Trace library calls made by a process (calls to shared libraries like libc). |
| `lsof` | List open files and the processes that have opened them; includes network sockets. |
| `fuser` | Identify processes using a file, directory, or socket. |
| `pmap` | Show memory map of a process, detailing memory regions and their usage. |

---

## System Information

| Command | Description |
|---------|-------------|
| `uname` | Print system information: kernel name, version, machine hardware, and OS. |
| `hostname` | Show or set the system's hostname (network name). |
| `hostnamectl` | Query or change the system hostname and related settings (systemd systems). |
| `uptime` | Show how long the system has been running, current time, users, and load averages. |
| `date` | Display or set the system date and time. |
| `timedatectl` | Query and change the system clock, timezone, and NTP synchronization settings. |
| `cal` | Display a calendar for the current month or a specified month/year. |
| `whoami` | Print the username of the currently logged-in user. |
| `who` | Show who is logged in to the system and from where. |
| `w` | Show who is logged in and what they are doing (processes running). |
| `id` | Print the UID, GID, and group memberships of the current or specified user. |
| `last` | Show the history of user logins and system reboots from /var/log/wtmp. |
| `lastlog` | Show the most recent login for each user on the system. |
| `lscpu` | Display detailed CPU architecture information: cores, threads, caches, flags. |
| `lsmem` | Show the ranges of available memory and their state. |
| `lshw` | List detailed hardware configuration of the machine. |
| `lspci` | List all PCI devices (graphics cards, network adapters, etc.). |
| `lsusb` | List all USB devices currently connected to the system. |
| `dmidecode` | Decode DMI/SMBIOS data to show hardware information from BIOS. |
| `dmesg` | Print or control the kernel ring buffer (boot messages, hardware errors). |
| `hwinfo` | Probe for and display detailed hardware information (may need installation). |
| `inxi` | Comprehensive system/hardware information tool (may need installation). |
| `arch` | Print the machine hardware architecture (e.g., x86_64, aarch64). |
| `nproc` | Print the number of available processing units (logical CPUs). |

---

## Disk & Filesystem

| Command | Description |
|---------|-------------|
| `df` | Report disk space usage for filesystems. -h gives human-readable sizes. |
| `du` | Estimate file space usage for files and directories. -sh gives a summary. |
| `mount` | Mount a filesystem (attach a storage device to the directory tree). |
| `umount` | Unmount a mounted filesystem (detach it from the directory tree). |
| `fdisk` | Partition table manipulator for MBR disks: create, delete, modify partitions. |
| `gdisk` | Interactive partition table manipulator for GPT disks. |
| `parted` | Powerful disk partitioning tool supporting MBR and GPT. |
| `mkfs` | Build (format) a Linux filesystem on a device (e.g., mkfs.ext4, mkfs.xfs). |
| `fsck` | Check and repair a Linux filesystem; should be run on unmounted partitions. |
| `e2fsck` | Check and repair an ext2/ext3/ext4 filesystem. |
| `tune2fs` | Adjust tunable filesystem parameters on ext2/ext3/ext4 filesystems. |
| `blkid` | Locate or print block device attributes: UUID, filesystem type, label. |
| `lsblk` | List block devices (disks, partitions, loop devices) in a tree format. |
| `dd` | Convert and copy a file, often used for creating disk images or writing ISOs. |
| `sync` | Flush filesystem buffers: force pending writes to disk. |
| `swapoff` | Disable a swap space (file or partition). |
| `swapon` | Enable a swap space to extend virtual memory. |
| `mkswap` | Set up a Linux swap area on a device or file. |
| `btrfs` | Manage Btrfs filesystems: subvolumes, snapshots, balancing, scrubbing. |
| `zfs` | Manage ZFS pools and datasets (requires ZFS kernel module). |
| `lvdisplay` | Display information about LVM logical volumes. |
| `vgdisplay` | Display information about LVM volume groups. |
| `pvdisplay` | Display information about LVM physical volumes. |
| `lvcreate` | Create a logical volume in an existing LVM volume group. |
| `vgcreate` | Create a new LVM volume group from one or more physical volumes. |
| `pvcreate` | Initialize a disk or partition as an LVM physical volume. |
| `cryptsetup` | Manage disk encryption with dm-crypt/LUKS (create, open, close encrypted volumes). |
| `badblocks` | Search a device for bad (unreadable) blocks. |
| `hdparm` | Get or set hard disk parameters, including performance settings and security features. |
| `smartctl` | Control and monitor SMART-capable hard disks and SSDs; check disk health. |
| `ncdu` | NCurses-based interactive disk usage analyzer. |

---

## Networking

| Command | Description |
|---------|-------------|
| `ip` | Show and manipulate routing, network devices, interfaces, and tunnels (modern replacement for ifconfig). |
| `ifconfig` | Configure network interfaces: assign IP addresses, bring up/down interfaces (legacy). |
| `ping` | Send ICMP echo requests to a host to test reachability and measure round-trip time. |
| `ping6` | Send ICMPv6 echo requests to test IPv6 connectivity. |
| `traceroute` | Trace the network path (hops) packets take to reach a destination host. |
| `tracepath` | Trace path to a host, discovering MTU along the way (no root required). |
| `mtr` | Combines ping and traceroute into a real-time network diagnostic tool. |
| `nslookup` | Query DNS servers interactively to resolve hostnames and IP addresses. |
| `dig` | DNS lookup utility: perform detailed DNS queries and display full server responses. |
| `host` | Simple DNS lookup command that resolves hostnames to IP addresses and vice versa. |
| `whois` | Query WHOIS databases to find domain registration and IP ownership information. |
| `curl` | Transfer data from/to URLs using many protocols (HTTP, HTTPS, FTP, etc.). |
| `wget` | Non-interactive network downloader; retrieve files from the web recursively. |
| `netstat` | Display network connections, routing tables, interface statistics (legacy, use ss). |
| `ss` | Socket statistics: show listening and established connections (modern netstat). |
| `nmap` | Network mapper: scan hosts for open ports, running services, and OS detection. |
| `arp` | View and manipulate the ARP cache (IP-to-MAC address mappings). |
| `route` | Show and manipulate the IP routing table (legacy; use ip route). |
| `iptables` | Configure IPv4 packet filtering, NAT, and firewall rules in the Linux kernel. |
| `ip6tables` | Configure IPv6 packet filtering and firewall rules. |
| `ufw` | Uncomplicated Firewall: user-friendly frontend for iptables rule management. |
| `firewall-cmd` | Interface to the firewalld dynamic firewall manager. |
| `tcpdump` | Capture and analyze network packets on an interface; a CLI packet analyzer. |
| `wireshark` | Graphical network protocol analyzer (CLI version: tshark). |
| `tshark` | Terminal-based Wireshark: capture and analyze network traffic from the command line. |
| `nc` | Netcat: read/write data across TCP/UDP connections; the 'Swiss Army knife' of networking. |
| `socat` | Bidirectional data relay between two data streams (more powerful than nc). |
| `ssh` | Secure Shell: open an encrypted remote login session or execute remote commands. |
| `scp` | Securely copy files between hosts over an SSH connection. |
| `sftp` | Interactive secure file transfer over SSH. |
| `rsync` | Fast, versatile file synchronization and transfer tool (local or remote via SSH). |
| `ftp` | File Transfer Protocol client for transferring files to/from FTP servers (unencrypted). |
| `telnet` | Connect to a remote host via Telnet (unencrypted; avoid for production, use for testing). |
| `nmcli` | NetworkManager command-line interface: manage connections, devices, and Wi-Fi. |
| `nmtui` | Text-based UI for NetworkManager (interactive TUI). |
| `iwconfig` | Configure wireless network interface parameters (legacy, use iw). |
| `iw` | Show or manipulate wireless devices and their configuration. |
| `iwlist` | Get detailed wireless information from a network interface (scan, frequency, etc.). |
| `hostapd` | Host access point daemon: turn a wireless interface into a Wi-Fi access point. |
| `dhclient` | DHCP client: request IP address assignment from a DHCP server. |
| `nftables` | Next-generation packet filtering framework and replacement for iptables. |
| `vnstat` | Network traffic monitor that keeps a log of network statistics. |
| `iftop` | Display real-time bandwidth usage on a network interface by connection. |
| `nethogs` | Show real-time network usage per process (which program is using bandwidth). |
| `ethtool` | Query and control network driver and hardware settings. |
| `iperf3` | Measure maximum achievable network bandwidth between two hosts. |
| `ab` | Apache HTTP server benchmarking tool: measure web server performance. |
| `openssl` | Toolkit for TLS/SSL protocols and cryptography: generate keys, certificates, encrypt files. |
| `gpg` | GNU Privacy Guard: encrypt, decrypt, sign, and verify files using public-key cryptography. |

---

## User & Group Management

| Command | Description |
|---------|-------------|
| `useradd` | Create a new user account with default or specified settings. |
| `usermod` | Modify an existing user account (change name, groups, home directory, shell, etc.). |
| `userdel` | Delete a user account and optionally their home directory and mail spool. |
| `passwd` | Change a user's password or set password aging policies. |
| `groupadd` | Create a new group on the system. |
| `groupmod` | Modify an existing group (rename, change GID, etc.). |
| `groupdel` | Delete a group from the system. |
| `gpasswd` | Administer /etc/group and /etc/gshadow: add/remove users from groups, set passwords. |
| `su` | Switch user: open a shell as another user, defaulting to root. |
| `sudo` | Execute a command as the superuser or another user, as permitted by /etc/sudoers. |
| `visudo` | Safely edit the /etc/sudoers file with syntax checking. |
| `chpasswd` | Update user passwords in batch from standard input. |
| `newgrp` | Change the current group ID during a login session. |
| `groups` | Print the names of the groups a user belongs to. |
| `finger` | Display information about system users (name, login, shell, idle time). |
| `chsh` | Change the login shell for a user. |
| `chfn` | Change user information (full name, phone numbers) stored in /etc/passwd. |
| `vipw` | Safely edit the /etc/passwd file with locking. |
| `vigr` | Safely edit the /etc/group file with locking. |
| `lid` | List the groups a user is a member of, or users who belong to a group. |
| `faillock` | Display or reset failed authentication attempt records. |
| `pam_tally2` | Display or reset the login failure count for a user (PAM module tool). |

---

## Package Management

| Command | Description |
|---------|-------------|
| `apt` | Advanced Package Tool: install, update, and remove packages on Debian/Ubuntu. |
| `apt-get` | Lower-level Debian package management tool; predates apt but still widely used. |
| `apt-cache` | Query the APT package cache for information about packages. |
| `dpkg` | Low-level Debian package manager: install, remove, and query .deb packages. |
| `snap` | Install and manage Snap packages (containerized, cross-distro application packages). |
| `flatpak` | Install and manage Flatpak applications in sandboxed environments. |
| `dnf` | Dandified YUM: package manager for Fedora/RHEL/CentOS (modern replacement for yum). |
| `yum` | Yellowdog Updater Modified: package manager for older RHEL/CentOS systems. |
| `rpm` | RPM Package Manager: install, query, verify, and erase RPM packages. |
| `pacman` | Arch Linux package manager: install, update, remove, and search packages. |
| `yay` | AUR (Arch User Repository) helper that wraps pacman for AUR package management. |
| `paru` | Another AUR helper with additional features and a Rust implementation. |
| `zypper` | openSUSE package manager: install, update, remove packages and manage repositories. |
| `emerge` | Gentoo package manager (Portage): compile and install software from source. |
| `nix` | Nix package manager: purely functional package management for NixOS and other distros. |
| `brew` | Homebrew: package manager primarily for macOS, also available on Linux. |
| `pip` | Python package installer: install packages from PyPI. |
| `pip3` | Python 3 version of pip. |
| `npm` | Node.js package manager: install JavaScript packages from npmjs.com. |
| `cargo` | Rust package manager and build tool: compile and manage Rust crates. |
| `gem` | RubyGems package manager: install Ruby libraries and applications. |
| `cpan` | CPAN shell: download and install Perl modules from CPAN. |

---

## Shell & Scripting

| Command | Description |
|---------|-------------|
| `bash` | Bourne Again SHell: the most common Linux shell, executes commands and scripts. |
| `sh` | POSIX-compatible shell (often symlinked to dash or bash on Linux). |
| `zsh` | Z Shell: feature-rich interactive shell with powerful completion and theming. |
| `fish` | Friendly Interactive SHell: user-friendly shell with autosuggestions and syntax highlighting. |
| `echo` | Print text or variable values to standard output. |
| `printf` | Format and print data, similar to C's printf; more control than echo. |
| `read` | Read a line of input from standard input into a variable. |
| `export` | Mark a shell variable for export to child processes as an environment variable. |
| `unset` | Remove a shell variable or function from the environment. |
| `set` | Display or set shell options and positional parameters. |
| `env` | Display or modify the environment for a command; print all environment variables. |
| `printenv` | Print the values of specified environment variables, or all if none specified. |
| `source` | Execute commands from a file in the current shell (same as the . built-in). |
| `alias` | Create a shortcut name for a longer command or set of commands. |
| `unalias` | Remove a previously defined alias. |
| `history` | Display the command history list for the current shell session. |
| `fc` | Fix command: edit and re-execute commands from history. |
| `type` | Indicate how a command name would be interpreted (builtin, alias, file, etc.). |
| `which` | Locate a command by searching the PATH and return its full path. |
| `whereis` | Locate the binary, source, and manual page files for a command. |
| `command` | Execute a command, bypassing shell functions and aliases. |
| `builtin` | Execute a shell built-in command, bypassing any defined function with the same name. |
| `test` | Evaluate conditional expressions; used in shell scripts for comparisons. |
| `expr` | Evaluate expressions (arithmetic, string, and logical) in a shell. |
| `let` | Evaluate arithmetic expressions in bash. |
| `declare` | Declare variables and give them attributes in bash. |
| `local` | Declare a variable as local in scope to a shell function. |
| `return` | Exit a shell function and return a value to the calling context. |
| `exit` | Exit the current shell or script with an optional exit status code. |
| `trap` | Catch and handle signals or other events in a shell script. |
| `true` | Do nothing and exit with a status of 0 (success). Useful in shell logic. |
| `false` | Do nothing and exit with a status of 1 (failure). Useful in shell logic. |
| `xargs` | Build and execute command lines from standard input. |
| `tee` | Read from stdin and write to both stdout and one or more files simultaneously. |
| `exec` | Replace the current shell process with a specified command, or redirect file descriptors. |
| `eval` | Concatenate arguments into a single command and execute it in the current shell. |
| `getopts` | Parse positional parameters (options) passed to a shell script. |
| `shift` | Shift positional parameters to the left by N positions in a script. |
| `basename` | Return just the filename component of a path (built-in or command). |
| `mapfile` | Read lines from stdin into an indexed array variable in bash. |

---

## Text Processing

| Command | Description |
|---------|-------------|
| `grep` | Search for lines matching a regex pattern in files or standard input. |
| `sed` | Stream editor for filtering and transforming text. |
| `awk` | Pattern-scanning and processing language for structured text. |
| `cut` | Remove sections (columns) from each line of input. |
| `paste` | Merge corresponding lines of files horizontally. |
| `sort` | Sort lines of text files lexicographically or numerically. |
| `uniq` | Report or omit repeated adjacent lines in sorted input. |
| `tr` | Translate or delete characters from standard input. |
| `wc` | Count lines, words, and bytes in files. |
| `diff` | Compare files line by line and show differences. |
| `comm` | Compare two sorted files line by line, showing lines unique to each. |
| `cmp` | Compare two files byte by byte and report the first difference. |
| `strings` | Find and print printable strings in binary files. |
| `iconv` | Convert text from one character encoding to another (e.g., UTF-8 to ISO-8859-1). |
| `recode` | Convert files between character sets and usages. |
| `dos2unix` | Convert Windows-style line endings (CRLF) to Unix-style (LF). |
| `unix2dos` | Convert Unix-style line endings (LF) to Windows-style (CRLF). |
| `tput` | Initialize terminal or query the terminfo database for terminal capabilities. |

---

## System Monitoring & Performance

| Command | Description |
|---------|-------------|
| `top` | Real-time dynamic process viewer showing CPU, RAM, and process info. |
| `htop` | Enhanced interactive process viewer with color and mouse support. |
| `atop` | Advanced system and process monitor with historical recording capability. |
| `glances` | Cross-platform system monitoring tool with a web interface option. |
| `iostat` | Report CPU and I/O statistics for devices and partitions. |
| `vmstat` | Report virtual memory, processes, paging, block I/O, traps, and CPU activity. |
| `mpstat` | Report per-processor and global CPU statistics. |
| `sar` | Collect, report, or save system activity information (part of sysstat). |
| `free` | Display the amount of free and used memory (RAM and swap) in the system. |
| `uptime` | Show current time, how long the system has been running, and load averages. |
| `pidstat` | Report per-process CPU, memory, and I/O statistics. |
| `pstat` | Report system activity (varies by distribution). |
| `dstat` | Versatile resource statistics tool combining vmstat, iostat, netstat, etc. |
| `perf` | Performance analysis tool for Linux: profiling, tracing, and benchmarking. |
| `valgrind` | Memory debugging, memory leak detection, and profiling tool. |
| `gprof` | GNU profiler: analyze program performance from instrumented binaries. |
| `time` | Measure the total real, user, and system time consumed by a command. |
| `systemd-analyze` | Analyze systemd boot performance and critical chain. |
| `slabtop` | Display kernel slab cache information in real time. |
| `numactl` | Control NUMA (Non-Uniform Memory Access) policy for processes. |
| `taskset` | Set or retrieve the CPU affinity of a process (which CPUs it can run on). |
| `cpufreq-info` | Display CPU frequency scaling information. |
| `sensors` | Read hardware sensor data: temperatures, fan speeds, voltages. |
| `acpi` | Display ACPI information: battery, thermal zones, AC adapter status. |
| `powertop` | Analyze power consumption and optimize power usage on Linux systems. |
| `turbostat` | Report processor frequency, idle statistics, and power usage for x86 CPUs. |

---

## Boot & Init

| Command | Description |
|---------|-------------|
| `grub-install` | Install the GRUB bootloader to a device. |
| `update-grub` | Regenerate the GRUB configuration file (Debian/Ubuntu). |
| `grub-mkconfig` | Generate a GRUB configuration file. |
| `grub2-install` | Install GRUB 2 bootloader (used on RPM-based distros). |
| `systemctl` | Manage systemd services and units: start, stop, enable, disable, status. |
| `journalctl` | Query and display messages from the systemd journal log. |
| `init` | Initialize the system (process 1); switch runlevels on SysV init systems. |
| `telinit` | Change the SysV init runlevel. |
| `runlevel` | Print the previous and current SysV runlevel. |
| `reboot` | Reboot the system. |
| `poweroff` | Power off the machine. |
| `halt` | Halt the system without powering off. |
| `shutdown` | Schedule a system shutdown or reboot with optional message to users. |
| `wall` | Send a message to all logged-in users' terminals. |
| `dmesg` | Print kernel boot messages and hardware detection output from the ring buffer. |
| `dracut` | Tool to generate an initramfs image for early boot. |
| `mkinitcpio` | Arch Linux tool to create an initial ramdisk environment (initramfs). |
| `kexec` | Load and boot a new kernel without going through the BIOS/UEFI firmware. |

---

## Security & Cryptography

| Command | Description |
|---------|-------------|
| `ssh-keygen` | Generate, manage, and convert SSH authentication keys. |
| `ssh-copy-id` | Copy a public SSH key to a remote host's authorized_keys file. |
| `ssh-agent` | Hold private keys in memory for passwordless SSH authentication. |
| `ssh-add` | Add private keys to the ssh-agent for passwordless authentication. |
| `openssl` | Cryptography toolkit: TLS/SSL, key generation, certificates, encryption, hashing. |
| `gpg` | GNU Privacy Guard: public-key encryption, signing, and key management. |
| `gpg2` | Version 2 of GPG with improved architecture and smartcard support. |
| `md5sum` | Compute and check MD5 message digests for file integrity verification. |
| `sha1sum` | Compute and check SHA-1 checksums (deprecated for security use). |
| `sha256sum` | Compute and check SHA-256 checksums for file integrity. |
| `sha512sum` | Compute and check SHA-512 checksums (stronger than SHA-256). |
| `base64` | Encode or decode data in Base64 format. |
| `uuencode` | Encode a binary file into printable ASCII for transmission. |
| `uudecode` | Decode a uuencoded file back to binary. |
| `chroot` | Run a command or shell with a different root directory (isolation technique). |
| `setenforce` | Set SELinux to enforcing or permissive mode. |
| `getenforce` | Print the current SELinux enforcement mode. |
| `sestatus` | Show the status of SELinux: mode, policy, booleans. |
| `aa-status` | Show AppArmor module status and loaded profiles. |
| `lynis` | Security auditing and hardening tool for Linux/Unix systems. |
| `auditctl` | Control the Linux audit system: add/remove audit rules. |
| `ausearch` | Search the Linux audit logs for specific events. |
| `fail2ban-client` | Control the fail2ban intrusion prevention service. |
| `nft` | Administration tool for the nftables packet filtering framework. |
| `cryptmount` | Mount encrypted filesystems without needing root privileges. |
| `veracrypt` | Disk encryption software for creating encrypted volumes/containers. |
| `age` | Simple, modern file encryption tool with small key sizes. |
| `pass` | Standard Unix password manager using GPG encryption and git. |
| `keepassxc` | Cross-platform password manager storing passwords in an encrypted database. |

---

## Development & Debugging

| Command | Description |
|---------|-------------|
| `gcc` | GNU C Compiler: compile C (and C++) source code into executables or object files. |
| `g++` | GNU C++ Compiler: compile C++ source code. |
| `make` | Build automation tool that reads a Makefile to compile projects. |
| `cmake` | Cross-platform build system generator that produces Makefiles or IDE projects. |
| `gdb` | GNU Debugger: debug programs, set breakpoints, inspect variables at runtime. |
| `lldb` | LLVM debugger: modern debugger with a Python API and Xcode integration. |
| `clang` | C/C++/Objective-C compiler from the LLVM project, known for helpful error messages. |
| `python3` | Run Python 3 scripts or launch the interactive Python interpreter. |
| `python` | Run Python scripts (may point to Python 2 or 3 depending on the system). |
| `node` | Execute JavaScript code using the Node.js runtime environment. |
| `java` | Run compiled Java programs using the JVM. |
| `javac` | Compile Java source files into bytecode. |
| `rustc` | Rust compiler: compile Rust source code into binaries. |
| `go` | Run, compile, test, and manage Go programs and modules. |
| `perl` | Run Perl scripts; powerful for text processing and system administration. |
| `ruby` | Run Ruby scripts or launch the interactive Ruby interpreter. |
| `php` | Run PHP scripts from the command line. |
| `lua` | Run Lua scripts; lightweight scripting language often embedded in applications. |
| `git` | Distributed version control system: track changes, branch, merge, collaborate. |
| `svn` | Apache Subversion: centralized version control system. |
| `hg` | Mercurial: distributed version control system (alternative to git). |
| `strace` | Trace system calls and signals; useful for debugging process behavior. |
| `ltrace` | Trace library function calls made by a process. |
| `nm` | List symbols from object files (functions, variables defined or used). |
| `objdump` | Display information about object files: disassembly, headers, symbols. |
| `readelf` | Display detailed information about ELF format binary files. |
| `strip` | Remove symbol table and debug information from binary files (reduces size). |
| `ar` | Create, modify, and extract from static library archives (.a files). |
| `ld` | GNU linker: link object files and libraries to create executables. |
| `ldd` | Print shared library dependencies of an executable or shared library. |
| `pkg-config` | Return information about installed libraries (compiler flags, linker flags). |
| `ctags` | Generate an index (tag) file of language objects for use by text editors. |
| `cscope` | Browse C/C++/Java source code interactively. |
| `indent` | Format C source code according to a specified style. |
| `splint` | Statically check C programs for security vulnerabilities and coding errors. |
| `valgrind` | Memory error detector and profiler: find leaks, invalid accesses, race conditions. |
| `gprof` | Profile execution of a program compiled with -pg flag. |
| `gcov` | Code coverage tool: measure which lines of code are executed during tests. |
| `docker` | Build, run, and manage containerized applications using Docker. |
| `podman` | Daemonless container engine; drop-in replacement for Docker. |
| `kubectl` | Command-line tool for controlling Kubernetes clusters. |
| `ansible` | IT automation tool: configure systems and deploy applications using YAML playbooks. |
| `terraform` | Infrastructure-as-code tool for provisioning cloud and on-premises resources. |
| `vagrant` | Build and manage reproducible development environments using virtual machines. |

---

## Help & Documentation

| Command | Description |
|---------|-------------|
| `man` | Display the manual page for a command; the most important help system on Linux. |
| `info` | Read Info documents (GNU hypertext documentation system). |
| `help` | Display help for shell built-in commands. |
| `whatis` | Display a one-line description of a command from the manual page database. |
| `apropos` | Search the manual page database for commands matching a keyword. |
| `tldr` | Community-maintained simplified man pages with practical examples. |
| `man -k` | Search man page descriptions for a keyword (same as apropos). |
| `--help` | Most commands accept --help or -h flag to print a brief usage summary. |
| `pinfo` | Colorized info page reader with vi-like navigation. |
| `manpath` | Display the search path for manual pages. |
| `makewhatis` | Create or update the whatis database for man page searching. |
| `update-alternatives` | Maintain symbolic links for multiple versions of commands (Debian/Ubuntu). |
| `xdg-open` | Open a file or URL with the default application as configured by the desktop. |

---

## Miscellaneous Utilities

| Command | Description |
|---------|-------------|
| `clear` | Clear the terminal screen (move content off-screen). |
| `reset` | Reset the terminal to a sane state if display is corrupted. |
| `tput reset` | Reset terminal settings using the terminfo database. |
| `script` | Record a terminal session (all input and output) to a file. |
| `screen` | Terminal multiplexer: run multiple shell sessions in one terminal, detach/reattach. |
| `tmux` | Terminal multiplexer with split panes, windows, and session persistence. |
| `byobu` | Enhanced terminal multiplexer wrapper around screen or tmux. |
| `xterm` | Standard terminal emulator for X Window System. |
| `xclip` | Read from or write to X clipboard from the command line. |
| `xsel` | Read and write to the X selection (clipboard) from the command line. |
| `xdotool` | Simulate keyboard input and mouse activity; manipulate windows programmatically. |
| `notify-send` | Send desktop notifications from the command line. |
| `zenity` | Display GTK dialog boxes from shell scripts. |
| `dialog` | Display dialog boxes from shell scripts in terminal environments. |
| `whiptail` | Lightweight dialog box utility (uses ncurses). |
| `bc` | Arbitrary-precision calculator language with interactive and script modes. |
| `dc` | Reverse-polish desk calculator with arbitrary precision. |
| `factor` | Print the prime factorization of a number. |
| `seq` | Generate sequences of numbers. |
| `yes` | Repeatedly output a string (default 'y'); useful for automating confirmations. |
| `cal` | Display a calendar. |
| `cowsay` | Generate ASCII art of a cow (or other characters) saying a given message. |
| `fortune` | Print a random, hopefully interesting quote or saying. |
| `figlet` | Print large ASCII-art text banners from regular text. |
| `lolcat` | Concatenate files and apply rainbow coloring to the output. |
| `banner` | Print a large ASCII banner of given text (sysv-banner). |
| `toilet` | Display large colorful characters using various fonts (alternative to figlet). |
| `sl` | Display an ASCII art steam locomotive; runs when you mistype 'ls'. |
| `cmatrix` | Display a Matrix-like screensaver in the terminal. |
| `asciinema` | Record and share terminal sessions as lightweight text-based videos. |
| `ffmpeg` | Powerful multimedia framework for recording, converting, and streaming audio/video. |
| `convert` | ImageMagick tool to convert between image formats, resize, annotate images. |
| `mogrify` | ImageMagick in-place image transformation tool. |
| `identify` | Identify the format and characteristics of image files (ImageMagick). |
| `display` | Display an image or image sequence using ImageMagick. |
| `feh` | Lightweight image viewer and wallpaper setter. |
| `sxiv` | Simple X Image Viewer; minimal and fast. |
| `mpv` | Media player based on MPlayer/mplayer2; plays nearly any format. |
| `vlc` | VLC media player (command-line mode: cvlc or --no-video). |
| `mplayer` | Media player for Linux; predecessor to mpv. |
| `sox` | Sound exchange: process and convert audio files from the command line. |
| `aplay` | Play audio files using ALSA (Advanced Linux Sound Architecture). |
| `arecord` | Record audio using ALSA. |
| `paplay` | Play audio files through PulseAudio. |
| `pactl` | Control the PulseAudio sound server: list, set volume, switch sinks/sources. |
| `wpctl` | Control the WirePlumber/PipeWire session manager (volume, default devices). |
| `pw-play` | Play audio through PipeWire. |
| `pw-record` | Record audio through PipeWire. |
| `amixer` | Command-line ALSA mixer: adjust audio levels, mute, unmute. |
| `alsamixer` | ncurses-based ALSA mixer for interactive audio control. |
| `mpd` | Music Player Daemon: plays music in the background, controlled by clients. |
| `mpc` | Command-line client for MPD: add songs, control playback, manage playlists. |
| `cava` | Console-based Audio Visualizer for ALSA, PulseAudio, and PipeWire. |
| `lp` | Print a file to the default or specified printer. |
| `lpq` | Display the printer queue and status. |
| `lprm` | Remove print jobs from a printer queue. |
| `lpadmin` | Configure CUPS printer queues and classes. |
| `cups` | Common Unix Printing System: manage printers and print jobs. |
| `xrandr` | Set the size, orientation, and reflection of X screen outputs. |
| `arandr` | Graphical front-end for xrandr to configure multi-monitor setups. |
| `xset` | User preference utility for X: set screen blanking, keyboard repeat, etc. |
| `setxkbmap` | Set the keyboard layout and variant for X Window System. |
| `xmodmap` | Modify keymaps and pointer button mappings in X. |
| `xbacklight` | Set or get screen brightness via the backlight subsystem. |
| `brightnessctl` | Read and control device brightness (backlight, keyboard LEDs). |
| `bluetoothctl` | Interactive Bluetooth controller: pair, connect, and manage devices. |
| `rfkill` | Enable or disable wireless devices (Wi-Fi, Bluetooth) via the rfkill subsystem. |
| `inotifywait` | Wait for changes to files using the inotify API; useful in scripts. |
| `inotifywatch` | Gather filesystem access statistics using inotify. |
| `lsmod` | Show the status of currently loaded kernel modules. |
| `modprobe` | Add or remove kernel modules from the Linux kernel. |
| `rmmod` | Remove a module from the Linux kernel. |
| `insmod` | Insert a module into the Linux kernel. |
| `modinfo` | Show information about a Linux kernel module. |
| `depmod` | Generate a list of module dependencies (modules.dep). |
| `sysctl` | Configure kernel parameters at runtime via the /proc/sys interface. |
| `dkms` | Dynamic Kernel Module Support: build and install kernel modules automatically. |
| `update-initramfs` | Update or create the initial ramdisk for booting (Debian/Ubuntu). |
| `dracut` | Generate an initramfs image (used on RPM-based distributions). |
| `locale` | Get locale-specific information or display the current locale settings. |
| `localectl` | Query and change the system locale and keyboard layout settings (systemd). |
| `tzselect` | Interactively select a timezone. |
| `hwclock` | Read or set the hardware (BIOS/CMOS) clock. |
| `ntpdate` | Set the date and time via NTP (legacy; use timedatectl/chronyd). |
| `chronyc` | Command-line interface for the chrony NTP daemon. |
| `ntpq` | Query NTP servers and daemons. |
| `logrotate` | Rotate, compress, and mail log files automatically. |
| `rsyslog` | Rocket-fast syslog daemon for log management and forwarding. |
| `logger` | Make entries in the system log from the command line or shell scripts. |
| `last` | Show listing of last logged-in users. |
| `lastb` | Show bad (failed) login attempts. |
| `faillog` | Display or set failed login attempt counts. |
| `utmpdump` | Dump UTMP and WTMP files in raw format for analysis. |
| `xdg-user-dirs-update` | Update XDG user directories (Desktop, Downloads, etc.). |
| `update-mime-database` | Rebuild the MIME type database from installed XML files. |
| `update-icon-caches` | Rebuild icon theme caches. |
| `fc-cache` | Rebuild the font cache for fontconfig. |
| `fc-list` | List available fonts on the system. |
| `fc-match` | Match a font pattern and return the best matching font. |
| `debconf` | Debian configuration management system for packages. |
| `dpkg-reconfigure` | Reconfigure an already-installed Debian package. |
| `tasksel` | Debian/Ubuntu tool to install or remove groups of related packages. |

---
