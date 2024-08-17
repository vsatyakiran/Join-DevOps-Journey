---
layout: default
title: Day 4 - Introduction to Shell Scripting
---

# Day 4: Introduction to Shell Scripting

<div class="date">August 13, 2024</div>

Today, I delved into shell scripting and its applications in DevOps. Here's what I learned:

## What is Shell Scripting?

Shell scripting involves writing a series of commands for the shell to execute. It allows for automation of tasks, system administration, and more. 

We can write shell scripting using Linux, boto3 or many other ways.

## Why Use Shell Scripting?

- **Automation**: Simplifies repetitive tasks
- **Customization**: Tailors scripts to specific needs
- **System Administration**: Manages system configurations and settings
- **Monitoring**: Automates monitoring tasks


## Shell Scripting Basics

- Shell scripts start with a shebang: `#!/bin/bash` or `#!/bin/sh`
- Comments are denoted with `#`
- Common debugging and error handling:
  - `set -x`: Enable debug mode
  - `set -e`: Exit the script when there's an error
  - `set -o pipefail`: Address drawbacks of `set -e` when using pipes

## Useful Commands in Scripts

- `curl`: Retrieve data from URLs
- `wget`: Download files and store information in a log file
- `find`: Search the entire file system
- `sudo`: Execute commands with superuser privileges

## Key Concepts

- Pipes (`|`) are used to send output from one command to another
- Logging is crucial for debugging and monitoring scripts
- Crontab is used for scheduling tasks

## Interview Questions and Answers

1. What is your understanding of shell scripting? How to use in day to day uses?
    - Shell scripting involves writing a series of commands for the shell to execute. It can be used for automating repetitive tasks, system administration, and monitoring. For day-to-day use, I often write scripts to automate backups, monitor system resources, and deploy applications.
    - list commands that you use 

2. Write a simple shell script to list all the process?
    - Here's a simple script that lists all processes:
    ```bash
    #!/bin/bash
    ps -ef
    ```

3. Write a script to print only errors from a remote log?
    - To print only errors from a remote log, you can use `curl` to fetch the log file and `grep` to filter out errors. Here's an example:
    ```bash
    #!/bin/bash
    curl http://example.com/logfile.txt | grep "ERROR"
    ```

4. Write a shell script to print numbers divided by 3 & 5 , not 15
    - Here's a script that prints numbers divisible by 3 or 5 but not 15:
    ```bash
    #!/bin/bash
    for i in {1..100}; do
        if [ $((i % 3)) -eq 0 ] && [ $((i % 5)) -eq 0 ]; then
            continue
        elif [ $((i % 3)) -eq 0 ] || [ $((i % 5)) -eq 0 ]; then
            echo $i
        fi
    done
    ```

5. Write a script to print number of "S" in messissipi
    - Here's a script that counts the number of occurrences of "S" in "mississippi":
    ```bash
    #!/bin/bash
    echo "mississippi" | grep -o "S" | wc -l
    ```


6. What is crontab in Linux? can you provide an example of usage?
    - Crontab is a time-based job scheduler in Unix-like operating systems. It allows users to schedule tasks to run periodically at fixed times, dates, or intervals. Here's an example of a crontab entry to run a script every day at 3 AM:
    ```
    0 3 * * * /path/to/script.sh
    ```

7. How to open a read-only file?
    - You can open a file in read-only mode using the `vim` editor with the `-R` option:
    ```
    vim -R filename
    ```
    - Alternatively, you can use `less` or `cat` to view the contents of a file without editing it. 

8. What is the difference between soft and hard link?
    - Soft links (symbolic links) are pointers to the original file, while hard links are direct references to the file's inode. Soft links can span file systems, while hard links cannot. Deleting the original file breaks a soft link, but not a hard link.

9. What are advantages and disadvantages of shell scripting?
    - Advantages:
      - Automates repetitive tasks
      - Customizes scripts for specific needs
      - Manages system configurations
      - Automates monitoring tasks
    - Disadvantages:
      - Limited error handling
      - Debugging can be challenging
      - Security risks if not properly secured
      - Performance overhead for complex scripts


10. Loops in shell scripting:
    - Loops in shell scripting allow you to iterate over a list of items or perform a set of commands repeatedly. Common loop types include `for`, `while`, and `until` loops. Here's an example of a `for` loop:
    ```bash
    #!/bin/bash
    for i in {1..5}; do
        echo "Iteration $i"
    done
    ```

11. What is bash? is it dynamic or statically typed and why?
    - Bash (Bourne Again Shell) is a Unix shell and command language that is widely used in Linux and other Unix-like operating systems. It is dynamically typed, meaning that variables do not have a fixed type and can change during runtime. This flexibility allows for easier scripting and handling of different data types.


12.Explain about a network troubleshooting utility?
    - Network troubleshooting utilities help diagnose and resolve network issues. Common utilities include:
      - `ping`: Tests network connectivity
      - `nslookup`: Queries DNS servers for domain information
      - `netstat`: Displays network connections, routing tables, and interface statistics
      - `traceroute`: Traces the route packets take to a destination
      - `tcpdump`: Captures and analyzes network traffic
      - `nmap`: Scans for open ports and services on a network
      - `ip`: Manages network interfaces, routing, and tunnels

13. How will you sort list of names in a file?
    - To sort a list of names in a file, you can use the `sort` command:
    ```
    sort names.txt
    ```
    - By default, `sort` sorts lines alphabetically. You can use options like `-r` for reverse sorting, `-n` for numerical sorting, and `-k` to specify a key for sorting.

14. How will you manage logs of a system that generate huge log files everyday?
    - To manage logs of a system that generate huge log files every day, you can use log rotation and log management tools. Log rotation involves archiving, compressing, and deleting old log files to save disk space. Tools like `logrotate`, `rsyslog`, and `syslog-ng` help automate log rotation and management tasks.

15. How to check disk space usage in Linux?
    - To check disk space usage in Linux, you can use the `df` command:
    ```
    df -h
    ```
    - The `-h` option displays disk space in human-readable format (e.g., GB, MB). You can also use `du` to check disk usage at the directory level.

## Key Takeaways

- Shell scripting automates tasks, system administration, and monitoring.
- Understanding basic shell scripting concepts is essential for DevOps work.
- Logging, error handling, and scheduling are crucial aspects of shell scripting.
- Practice and experimentation are key to mastering shell scripting.

## Challenges Faced

- Remembering the syntax and options for various commands can be overwhelming.
- Debugging complex scripts and handling errors effectively require practice.

## Resources Used

- [YouTube: Abhishek Veeramalla](https://www.youtube.com/playlist?list=PLdpzxOOAlwvIKMhk8WhzN1pYoJ1YU8Csa)

## Next Steps

- Practice writing more complex shell scripts for real-world scenarios.
- Explore advanced shell scripting techniques and best practices.
- Learn about shell scripting security and secure coding practices.

<div class="navigation">
  <a href="../logs/day-3.md" class="btn">Previous Day</a>
  <a href="../index.md" class="btn">Back to Home</a>
  <a href="../logs/day-5.md" class="btn">Next Day</a>
</div>
