# ansible-motd

Ansible role to manage MOTD

[motd](<https://en.wikipedia.org/wiki/Motd_(Unix)>)

## Build Status

### GitHub Actions

![Molecule Test](https://github.com/mrlesmithjr/ansible-motd/workflows/Molecule%20Test/badge.svg)

### Travis CI

[![Build Status](https://travis-ci.org/mrlesmithjr/ansible-motd.svg?branch=master)](https://travis-ci.org/mrlesmithjr/ansible-motd)

## Requirements

For any required Ansible roles, review:
[requirements.yml](requirements.yml)

## Role Variables

[defaults/main.yml](defaults/main.yml)

## Dependencies

## Example Playbook

[playbook.yml](playbook.yml)

## Example MOTD

`custom:`

> NOTE: This is the default

```bash
System Information for node0 on Thu Jun 22 04:53:54 UTC 2017
================================================================================
CPU Load              : 1%
CPU Usage             :
%Cpu(s): 10.2 us,  2.5 sy,  0.0 ni, 86.5 id,  0.6 wa,  0.0 hi,  0.3 si,  0.0 st

Top 5 Processes(CPU)  :
USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root         1  0.1  0.9 184952  4896 ?        Ss   04:46   0:00 /sbin/init
root         2  0.0  0.0      0     0 ?        S    04:46   0:00 [kthreadd]
root         3  0.0  0.0      0     0 ?        S    04:46   0:00 [ksoftirqd/0]
root         4  0.0  0.0      0     0 ?        S    04:46   0:00 [kworker/0:0]
root         5  0.0  0.0      0     0 ?        S<   04:46   0:00 [kworker/0:0H]

Memory Total          : 488M
Memory Free           : 180M
Memory Buffer/Cache   : 280M
Memory Usage          : 0.2%
Swap Usage            : 0.2%

Disk Mounts           :
Filesystem                   Type      Size  Used Avail Use% Mounted on
/dev/mapper/vagrant--vg-root ext4       35G  1.8G   31G   6% /
/dev/sda1                    ext2      472M  100M  348M  23% /boot
vagrant                      vboxsf    465G  165G  301G  36% /vagrant

IP Addresses          :
[enp0s3/UP]: 10.0.2.15
[enp0s8/UP]: 192.168.250.10

DNS Servers           : 10.0.2.3
DNS Response Time     : 19 msec



Last login: Thu Jun 22 04:53:05 2017 from 10.0.2.2
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

MIT

## Author Information

Larry Smith Jr.

- [@mrlesmithjr](https://twitter.com/mrlesmithjr)
- [mrlesmithjr@gmail.com](mailto:mrlesmithjr@gmail.com)
- [http://everythingshouldbevirtual.com](http://everythingshouldbevirtual.com)

> NOTE: Repo has been created/updated using [https://github.com/mrlesmithjr/cookiecutter-ansible-role](https://github.com/mrlesmithjr/cookiecutter-ansible-role) as a template.
