# CentOS-7-x86_64-DVD-Provisioning
Init script for CentOS 7 - Configure static IP, Fail2Ban, Docker, etc.

----------------------------------------------------------------------------------------------

**Table of Contents**

- [Summary](#summary)
- [Requirements](#requirements)
- [Getting Started](#getting-started)
- [Configurations and Default values](#configurations-and-default-values)
- [Packages](#packages)


# Summary
A basic init script for getting Docker up and running in CentOS 7. Provides an interactive prompt
for configuring network information and utilizes Fail2Ban to thwart SSH intrusion.

# Requirements
1. CentOS-7-x86_64-DVD.iso (Minimal install not currently supported)
2. Root privilege

# Getting Started
Install CentOS-7-x86_64-DVD.iso and run `./init.sh`. Provide information for Time Zone and Network config. First run may take some time as multiple packages are configured for update.

# Configurations and Default values
1. Time Zone: America/New_York
2. Static IP and CIDR: 192.168.1.100/24
3. Gateway: 192.168.1.1
4. DNS1: 192.168.1.1
5. DNS2: 8.8.8.8
6. Hostname: centos7-docker
7. SSH root access disabled
8. SSH retries limited to 3 per 10 minutes with 10 minute ban

# Packages
1. epel-release
2. nmap
3. fail2ban
4. docker-engine
5. docker-compose
