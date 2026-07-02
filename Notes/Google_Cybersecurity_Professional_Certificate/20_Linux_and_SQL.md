Linux and SQL


Operating System Interfaces

User Interface: A program that allows a user to control the core functions of an operating system.

    (Context: Translates human inputs into computer execution routines.)

Graphical User Interface (GUI): A visual user interface that relies on graphical icons, menus, windows, and pointer interactions to manage different tasks on a computer.

    (Context: Standard environments package a desktop workspace with shortcuts, a taskbar, and a start menu. While intuitive for beginners, it lacks automation velocity for repetitive administrative tasks.)

Command-Line Interface (CLI): A text-based user interface that processes explicit written commands to interact directly with the computer.

    (Context: Far more flexible and powerful than a GUI. A CLI allows advanced configuration, environment customization, and high-velocity scripting to execute multiple complex tasks simultaneously.)

Defensive & Administrative Advantages of a CLI

Operational Efficiency: A CLI can execute bulk administrative workflows in seconds using single-line inputs (such as generating hundreds of structured log directories instantly), which would otherwise require tedious, repetitive mouse clicks in a GUI.

Forensic History Tracking: The Linux CLI natively records a persistent history file documenting every command string and utility action executed inside the shell session.

    (Context: Crucial for incident response teams verifying triage steps from a playbook. If a system is compromised, investigators can analyze this history file to trace the adversary's post-exploitation footprints.)

Linux Architecture Basics

Linux Operating System: An open-source operating system developed in the early 1990s as a combination of independent projects to improve computer engineering.

    (Context: Created by Linus Torvalds to be open and accessible, it is the most-used operating system in security today because it allows direct access to the underlying source code and operating environment.)

Linux Core Architecture: The structural configuration of a Linux-based system, divided into six distinct operating layers working in tandem.

    The User: The person actively interacting with the computer.

    Applications: Programs designed to execute specific tasks, such as a word processor or a calculator.

    The Shell: The text-based environment layer that sits between application processes and the core operating infrastructure; this is how you communicate with the system.

    Filesystem Hierarchy Standard (FHS): The structural standard that defines the organization of files, directories, and paths inside the system storage layer.

    The Kernel: The core component of the Linux OS that manages processes and memory. Torvalds' revolutionary design uses built-in drivers to enable applications to execute hardware tasks, ensuring the system allocates resources efficiently and runs faster.

    Hardware: The raw physical components of a computer (CPU, RAM, motherboard).

Linux Distributions (Distros)

Linux Distribution (Distro): An operating system made by a software manufacturer or community that takes the core Linux kernel and packages it alongside custom user interfaces, shells, libraries, and application utilities.

    (Context: This is comparable to an auto manufacturer taking a baseline engine (the kernel) and building different vehicles (trucks, cars) around it. Major software families dictate lineage: Red Hat is the parent of CentOS, Slackware is the parent of SUSE, and Debian serves as the common ancestral baseline for many widely used security operating systems.)

    Kali Linux: A specialized open-source distribution derived from Debian, created by Offensive Security explicitly for penetration testing and digital forensics.

        (Context: Must strictly be run inside an isolated virtual machine (VM) rather than directly on host hardware to prevent host damage. It includes a massive suite of built-in tooling for proactive security testing and digital forensics:)

        Metasploit: An exploitation framework used to search for, audit, and systematically exploit documented weaknesses on target machines.

        Burp Suite: A specialized tool designed to intercept, modify, and test for flaws inside web application protocols.

        John the Ripper: A high-velocity password security cracking tool used to run brute-force and dictionary guesses against user hashes.

        Digital Forensics Suite: Features pre-installed investigative modules used to preserve and reconstruct data patterns after an intrusion event occurs. This includes command-line tools like tcpdump to capture live packet traffic, graphical analyzers like Wireshark to dissect recorded protocol headers, and deep disk suites like Autopsy to forensically examine compromised hard drives or smartphones.

    Ubuntu: A highly popular, open-source, user-friendly Debian-derived distribution heavily deployed in cloud computing environments and general IT management.

        (Context: Features both a functional GUI and a robust CLI out-of-the-box. Includes a massive public repository package manager to easily download custom security tools. As companies shift workflows into enterprise cloud clusters, security personnel frequently interact with Ubuntu server instances.)

    Parrot OS: A Debian-derived open-source distribution designed for security teams that pairs an accessible graphical workspace with pre-installed penetration testing and digital forensics packages.

    Red Hat Enterprise Linux (RHEL): A commercial, subscription-based distribution built strictly for enterprise architectures, providing managed software baselines and a dedicated vendor support desk to resolve infrastructure failures.

    AlmaLinux: A community-driven, open-source Linux distribution engineered to serve as a 1-to-1 binary drop-in replacement for CentOS (CentOS 8 reached End-of-Life in December 2021 after using upstream Red Hat code). It guarantees that existing corporate application configurations remain stable without alteration.

Shell Subsystems & Standard Streams

Linux Shell Interface: The command interpreter that reads user text commands and transforms them into executable kernel routines.

    (Context: Shell variants use different terminal characters to prompt user input. For instance, the Korn Shell (ksh) and the Bourne-Again Shell (bash) use a dollar sign ($) as their line prompt header, while the Z Shell (zsh) relies on a percent symbol (%).)

    Bourne-Again Shell (Bash): The default and most popular command shell packaged inside standard Linux distributions, heavily leveraged by security analysts to run basic commands, script automation routines, and pipe system updates.

Standard I/O Streams: The foundational text channels used by Linux applications and shells to pass parameters, render logs, and intercept data.

    Standard Input (stdin): The stream of data or information received by the operating system directly from user command-line parameters or interactive keyboard hooks.

    Standard Output (stdout): The clean informational stream returned by the operating system to display successful command results through the shell viewport.

        (Context: Demonstrated via the echo command, a core utility that accepts target string data—an ordered sequence of text characters—via standard input and echoes it directly back to the terminal viewport via standard output.)

    Standard Error (stderr): A dedicated, completely separate data stream reserved to process and print error codes or execution fault logs returned by the operating system when a command failure occurs.

Linux File Permissions & Access Control

Linux File Permissions: A 10-character metadata string that defines read, write, and execute capabilities across three distinct tiers of system owners.

    (Context: Managing permissions properly enforces the Principle of Least Privilege, ensuring users hold only the minimal level of system access required to complete their designated tasks. Lax permission structures allow threat actors to perform post-exploitation privilege escalation or read sensitive files.)

    Permission Operational Types:

        Read (r): For files, the power to read file contents; for directories, the power to list all items contained within (including files and subdirectories).

        Write (w): For files, the power to modify contents; for directories, the power to create new files within.

        Execute (x): For files, the power to execute the file if it is a program binary; for directories, the power to change directory (cd) into it and access its files.

    Owner Category Tiers:

        User (u): The specific user account that owns the file or directory.

        Group (g): A larger group/collection of users that the owner is a part of.

        Other (o): All other user accounts or standard system processes on the operating system.

Dissecting the 10-Character Permission String:

    Character 1: Identifies file type (- for regular files, d for a directory structure).

    Characters 2–4: Defines Read (r), Write (w), and Execute (x) permissions explicitly for the User.

    Characters 5–7: Defines Read (r), Write (w), and Execute (x) permissions explicitly for the Group.

    Characters 8–10: Defines Read (r), Write (w), and Execute (x) permissions explicitly for Other.

    (Note: Missing or denied permissions are structurally represented by a hyphen character (-).)

Investigating Permissions via the CLI

    ls Command Options: Analysts leverage options on the list directory (ls) command to audit systemic files and flag weak access controls.

        ls -l: Renders a long list layout showing the full 10-character permission string, owner name, group, file size, and last modification timestamp.

        ls -a: Forces the shell to display hidden files (files prefixing a period character like .bash_history).

        ls -la: Combines both switches to output a detailed permission audit list that includes hidden assets.

Modifying Permissions via chmod

    chmod Utility: Changes file or directory authorization masks by updating the underlying permission metadata bits.

        (Context: Requires two distinct command arguments: the tactical modification parameters followed by the explicit target file path. Using the equal character (=) functions as an exact absolute assignment, resetting the permission mask and completely overwriting existing permissions—removing any existing, unspecified bits.)

Command Parameter Matrix for chmod:

    Owners: u (User) | g (Group) | o (Other)

    Operations: + (Grant/Add) | - (Revoke/Remove) | = (Set Absolute)

    Permission Bits: r (Read) | w (Write) | x (Execute)

Execution Example (Grant Full Permissions):
Bash

chmod u+rwx,g+rwx,o+rwx login_sessions.txt

Execution Example (Revoke All Privileges):
Bash

chmod u-rwx,g-rwx,o-rwx login_sessions.txt

Execution Example (Absolute Least-Privilege Reset):
Bash

chmod u=r,g=r,o=r login_sessions.txt
