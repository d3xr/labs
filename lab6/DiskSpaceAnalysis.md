# Disk Space and Resource Consumption Analysis

## Disk Space Analysis

I used the 'df -h' command to analyze the disk space in my operating system. Here is the output:

Filesystem      Size   Used  Avail Capacity iused      ifree %iused  Mounted on
/dev/disk1s5   233Gi   10Gi  111Gi     9%  487437 2446569443    0%   /
devfs          191Ki  191Ki    0Bi   100%     660          0  100%   /dev
/dev/disk1s1   233Gi  109Gi  111Gi    50% 1944597 2443996283    0%   /System/Volumes/Data
/dev/disk1s4   233Gi  1.0Gi  111Gi     1%       1 2445941880    0%   /private/var/vm
map auto_home    0Bi    0Bi    0Bi   100%       0          0  100%   /System/Volumes/Data/home

## Inodes Analysis

For analyzing the number of inodes, I used the 'df -i' command. Here is the output:

Filesystem     512-blocks     Used Available Capacity iused      ifree %iused  Mounted on
/dev/disk1s5   489620264 20971784 233971264     9%  487437 2446569443    0%   /
devfs                 382      382         0   100%     660          0  100%   /dev
/dev/disk1s1   489620264 22776528 233971264    50% 1944597 2443996283    0%   /System/Volumes/Data
/dev/disk1s4   489620264  2097336 233971264     1%       1 2445941880    0%   /private/var/vm
map auto_home          0        0         0   100%       0          0  100%   /System/Volumes/Data/home

## Resource Consumption Analysis

To identify the process consuming the most RAM and CPU, I used the 'top' command. The process consuming the most resources was Google Chrome, which isn't surprising given its reputation.

PID    COMMAND      %CPU TIME     #TH   #WQ  #PORT MEM    PURG   CMPRS  PGRP  PPID  STATE    BOOSTS           %CPU_ME %CPU_OTHRS UID  FAULTS    COW     MSGSENT    MSGRECV    SYSBSD      SYSMACH     CSW        PAGEINS IDLEW POWER USER
85489  Google Chrom 12.7 37:11.72 33/1  10   370   269M+  0B     62M-   85489 85119 running  *0[1]            0.00000 0.00000    501  528497+   329     328283+    139481+    1879295+    3462249+    235392+    2600+   0     100.0 jdoe
