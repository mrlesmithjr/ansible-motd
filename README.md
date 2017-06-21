# Role Name

An [Ansible] role to manage [MOTD]

## Requirements

None

## Role Variables

```yaml
---
# defaults file for ansible-motd

# Define custom scripts to install
motd_custom_scripts:
  - '30-sysinfo'

# Defines default directory for MOTD scripts
motd_default_dir: '/etc/update-motd.d'

# Defines a default message to apply above any custom messages
motd_default_message: ''

# Defines if all default MOTD scripts in motd_default_dir should be disabled
motd_disable_defaults: true

# Defines if custom motd script(s) are enabled
motd_enable_custom_scripts: true

# Defines if static configured motd info using Ansible facts is enabled
motd_static: false

# Defines default Ubuntu scripts
motd_ubuntu_defaults:
  - '00-header'
  - '10-help-text'
  - '91-release-upgrade'
```

## Dependencies

None

## Example Playbook

```yaml
---
- hosts: all
  become: true
  vars:
  roles:
    - role: ansible-motd
  tasks:
```

## Example MOTD

`custom:`

```bash
System Information for node0 on Wed Jun 21 20:03:18 UTC 2017
======================================================================================
CPU Load              : 0%
CPU Usage             :
%Cpu(s):  1.2 us,  0.4 sy,  0.0 ni, 98.3 id,  0.1 wa,  0.0 hi,  0.0 si,  0.0 st

Top 5 Processes(CPU)  :
USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
vagrant  19381  0.2  1.0  95368  5152 ?        S    20:03   0:00 sshd: vagrant@notty
root         1  0.0  1.0 185280  5268 ?        Ss   18:34   0:01 /sbin/init
root         2  0.0  0.0      0     0 ?        S    18:34   0:00 [kthreadd]
root         3  0.0  0.0      0     0 ?        S    18:34   0:00 [ksoftirqd/0]
root         5  0.0  0.0      0     0 ?        S<   18:34   0:00 [kworker/0:0H]

Memory Total          : 488M
Memory Free           : 166M
Memory Usage          : 0.2%
Swap Usage            : 0.2%

Disk Mounts           :
Filesystem                   Type      Size  Used Avail Use% Mounted on
/dev/mapper/vagrant--vg-root ext4       35G  1.8G   31G   6% /
/dev/sda1                    ext2      472M  100M  348M  23% /boot
vagrant                      vboxsf    465G  193G  273G  42% /vagrant

IP Addresses          : [enp0s3/UP]: 10.0.2.15 [enp0s8/UP]: 192.168.250.10
DNS Servers           : 10.0.2.3
DNS Response Time     : 3 msec



Last login: Wed Jun 21 20:02:03 2017 from 10.0.2.2
```

`Static:`

```bash
Last login: Tue Apr  4 22:36:34 2017 from 10.0.2.2

****************Ansible Managed MOTD****************
Welcome to your Dev Environment

System Information For Hostname: node0

Distribution: Fedora
Distribution Release: Twenty Five
Distribution Version: 25
DNS Search: etsbv.internal
DNS Server(s): 10.0.2.3
Interfaces: lo(127.0.0.1) eth1(192.168.250.10)(08:00:27:44:8a:09) eth0(10.0.2.15)(08:00:27:00:92:30)
Kernel: 4.8.6-300.fc25.x86_64
Memory Installed: 0.5GB
Memory Swapfile: 1.2GB
Mounts: Mount: /dev/sda3(/)(15.0GB) Mount: /dev/sda1(/boot)(1.0GB)
Processors: 1
Python Version: 2.7.13
Timezone: EDT(-0400)

************End Of Ansible Managed MOTD*************
```

## License

BSD

## Author Information

Larry Smith Jr.

-   @mrlesmithjr
-   <http://everythingshouldbevirtual.com>
-   mrlesmithjr [at] gmail.com

[ansible]: https://www.ansible.com

[motd]: https://en.wikipedia.org/wiki/Motd_(Unix)
