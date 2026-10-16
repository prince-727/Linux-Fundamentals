# Linux Fundamentals Assignment

This project explores fundamental Linux system administration and basic network connectivity using a Kali Linux virtual machine. It demonstrates how to retrieve system information, inspect hardware resources, identify the Linux kernel version, and test network connectivity using the `ping` command.

## Table of Contents

- Project Overview
- Network Topology
- Tools and Technologies
- Configuration Steps
- Results and Findings
- Author

## Project Overview

The purpose of this project is to develop practical skills in Linux fundamentals and basic network troubleshooting. The assignment focuses on two main areas:

- **System Information:** Identifying the current user, hostname, working directory, operating system details, memory capacity, disk space, and Linux kernel version.
- **Network Connectivity:** Testing connectivity to a known IP address and a domain name using the `ping` command, while analysing response times and packet loss.

The project provides hands-on experience with essential Linux commands and introduces basic methods for verifying internet connectivity and understanding network response times.

## Network Topology

The project uses a Kali Linux virtual machine to perform system information checks and network connectivity tests against external internet destinations.

**Network layout:**

`Kali Linux Virtual Machine` → `Internet Connection` → `External Network Destinations`

**Devices and network details:**

- **Client machine:** Kali Linux virtual machine.
- **Hostname:** `kali`.
- **Username:** `kali`.
- **Working directory:** Home directory.
- **External IP address tested:** `8.8.8.8`.
- **Domain name tested:** `google.com`.
- **Resolved IP address:** `92.249.39.135`.

The assignment does not specify the virtualisation platform, network adapter configuration, subnet mask, default gateway, or local IP address.

## Tools and Technologies

- **Kali Linux:** Linux distribution used for the practical exercises.
- **Linux Kernel:** Version `6.19.14`.
- **Virtual Machine (VM):** Environment in which Kali Linux was running.
- **Terminal:** Interface used to execute Linux commands.
- **`whoami`:** Displays the current username.
- **`hostname`:** Displays the machine's hostname.
- **`pwd`:** Displays the current working directory.
- **`ping`:** Tests network connectivity and measures round-trip response times.
- **`-c` option:** Specifies the number of ping requests to send before stopping.
- **Google Public DNS IP address (`8.8.8.8`):** External IP address used for a connectivity test.
- **`google.com`:** Domain name used to test domain resolution and connectivity.

## Configuration Steps

1. **Open the Kali Linux terminal.**

   Start the Kali Linux virtual machine and open a terminal to execute the required commands.

2. **Identify the current user.**

   Run the following command:

   ```bash
   whoami
   ```

   The output identifies the current username as `kali`.

3. **Check the hostname.**

   Execute:

   ```bash
   hostname
   ```

   The hostname displayed is `kali`.

4. **Check the current working directory.**

   Run:

   ```bash
   pwd
   ```

   The command confirms that the current working directory is the home directory.

5. **Inspect operating system and hardware information.**

   Retrieve the operating system and hardware details using the commands demonstrated in the assignment. The results indicate that the virtual machine has approximately `5.8 GiB` of RAM, `4.5 GiB` of available disk space on the main partition, and Linux kernel version `6.19.14`.

   The specific commands used for these checks are not documented in the assignment text.

6. **Test connectivity to an external IP address.**

   Execute:

   ```bash
   ping -c 2 8.8.8.8
   ```

   This sends two ICMP echo requests to `8.8.8.8` and displays the connectivity results and summary statistics.

7. **Test connectivity using a domain name.**

   Run:

   ```bash
   ping -c 4 google.com
   ```

   This sends four ICMP echo requests to `google.com`. The command also allows the system to resolve the domain name to an IP address.

8. **Analyse the ping results.**

   Review the resolved IP address, round-trip time, and packet-loss statistics for both connectivity tests. Compare the results to understand how response times can differ between network destinations.

## Results and Findings

The assignment successfully demonstrates basic Linux system identification and network connectivity testing.

**System information results:**

- **Username:** `kali`.
- **Hostname:** `kali`.
- **Working directory:** Home directory.
- **Total RAM:** `5.8 GiB`.
- **Available disk space:** `4.5 GiB` on the main partition.
- **Linux kernel version:** `6.19.14`.

**Network connectivity results:**

- **Ping destination:** `8.8.8.8`.
  - Command: `ping -c 2 8.8.8.8`.
  - Average round-trip time: `183.032 ms`.
  - Packet loss: `0%`.

- **Ping destination:** `google.com`.
  - Command: `ping -c 4 google.com`.
  - Resolved IP address: `92.249.39.135`.
  - Reported round-trip time: `56.252 ms`.

**Key findings:**

- The `whoami`, `hostname`, and `pwd` commands provide essential information about the current user, machine identity, and working location.
- The system information checks provide an overview of the virtual machine's memory, available disk space, and Linux kernel version.
- The ping test to `8.8.8.8` completed with `0% packet loss`, indicating successful delivery of the tested echo requests.
- The domain-based ping test demonstrated that `google.com` resolved to an IP address and returned network responses.
- The measured response time for `google.com` was lower than that for `8.8.8.8
