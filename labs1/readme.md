# Huawei Cloud Storage Services Lab Report

## Overview
This document provides a summarized walkthrough of the lab exercises completed using Huawei Cloud's key storage services: Elastic Volume Service (EVS), Object Storage Service (OBS), and Scalable File Service (SFS Turbo). The exercises focus on creating, managing, and verifying the behavior of each service using ECS instances.

---

## 1. Elastic Volume Service (EVS)

### Objectives
- Purchase and attach EVS disks
- Initialize disks on Windows and Linux ECSs
- Use EVS snapshots for backup and restore

### Windows ECS Tasks
1. **Create VPC and ECS**  
   - Region: AP-Singapore  
   - ECS Name: `ecs-vivi`, Windows Server 2012 R2

2. **Purchase EVS Disk**  
   - Size: 20 GB, High I/O, named `volume-vivi`

3. **Attach EVS Disk**  
   - Attached to `ecs-vivi`, confirmed status as "In-use"

4. **Initialize Disk**  
   - Initialized via Disk Management (MBR/GPT)  
   - Partitioned, formatted, and mounted

5. **Data Verification**  
   - Created file `test.txt`, detached disk, and attached to `ecs-test`  
   - Verified file presence on second ECS

### Linux ECS Tasks
1. **Create ECS and EVS Disk**  
   - ECS Name: Custom Linux instance (CentOS 7.6)  
   - Disk: `volume-linuxadd`

2. **Initialize and Mount Disk**  
   - Used `fdisk` to partition `/dev/vdb1`  
   - Formatted with `ext4`, mounted to `/mnt/sdc`  
   - Added UUID entry to `/e

