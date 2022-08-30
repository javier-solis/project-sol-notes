# File System Hierarchy
Typical GNU/Linux File System Hierarchy (FHS), simplified as much as possible, with relavent examples.

## `/bin`
**Full Name:** Binaries  
**Notes:**
* Essential command binaries reside here.
* These are available for all users.

**Example(s):** Things like _ls_ and _cat_ are here.


## `/sbin`
**Full Name:** System Binaries  
**Notes:**
* Only system administrators can edit these files (i.e. have `sudo` privileges)
* Contains binary executables.

**Example(s):** `reboot`, `fdisk`, `ifconfig`, etc.


## `/boot`
**Full Name:** Boot  
**Notes:**
* Contains everything OS needs to boot.
* Kernel initrd, vmlinux, and GRUB files are located here.
* 
**Example(s):** Files such as `initrd.img-2.6.32-24-generic`

## `/dev`
**Full Name:** Devices  
**Notes:**
* Where device files live.
* Includes terminal interfaces and devices _externally connected_ to your system.
* 
**Example(s):** On the hardware side, you can find the files related to disks and their partitions, USB peripherals, etc. You can also find the files for terminal interfaces, such as `/dev/tty1`.


## `/etc`
**Full Name:** Etcetera  
**Notes:**
* For system-wide configurations of apps.
* Contains files required by all programs.
* This also contains startup and shutdown shell scripts used to start and stop individual programs, respectively.

**Example(s):** n/a


## `/home`
**Full Name:** Home  
**Notes:**
* Contains the directories of individual users.

**Example(s):** `/home/linus`


## `/lib`
**Full Name:** Library  
**Notes:**
* Contains file applications that can be used to perform various functions.
* Libraries essential for the binaries in `/bin` and `/sbin` are here.
* Library filenames are either in `ld*` or `lib*.so.*` format.

**Example(s):** -


## `/mnt`
**Full Name:** Mount  
**Notes:**
* Where the system mounts removable media
* The data of flash drives can be found here.

**Example(s):** -


## `/media`
**Full Name:** Media  
**Notes:**
* Where users can mount devices manually

**Example(s):** -


## `/opt`
**Full Name:** Optional  
**Notes:**
* Where software from 3rd parties resides, as well as some repo packages.

**Example(s):** -


## `/proc`
**Full Name:** Processes  
**Notes:** 
* Here lies a virtual filesystem that contains process and kernel information in the form of files. This corresponds to a "procfs mount".
* Where you'd find pseudo files that contain information about running system processes and system resources.

**Example(s):**
* If you navigate to the system monitor you'll spot out process IDs. Those IDs exists as folders in `/proc`
* Contains CPU information
* Contains Uptime information


## `/root`
**Full Name:** Root  
**Notes:**
* Is the root user's home folder. 
* You need root permission to modify these contents.

**Example(s):** -


## `/run`
**Full Name:** Run  
**Notes:**
* It's a "tempfs" filesystem (i.e. runs in RAM, and everything here is wiped when your system shuts down).
* Stores volatile runtime data.

**Example(s):**


## `/snap`
**Full Name:** Snap  
**Notes:** 
* Where snap packages reside. These are mainly maintained by Ubuntu.

**Example(s):** -


## `/srv`
**Full Name:** Service  
**Notes:**
* Contains site-specific data served by your system, such as data, scripts for web servers, etc.

**Example(s):** -


## `/tmp`
**Full Name:** Temporary  
**Notes:**
* Contains files that are temporarily used by applications.
* Files under this directory are deleted when system shutsdown.
  
**Example(s):** The autosave feature of some applications often make use of this folder. 

## `/sys`
**Full Name:** System  
**Notes:**
* Interacts with the kernel. 
* Similar to `/run` in that it's temporary.
  
**Example(s):** - 


## `/usr`
**Full Name:** User (but also referred to as Unix Service Resource)  
**Notes:**
* Contains the majority of user utilities and applications.
* Apps here are considered non-essential for system operations.
* Specific sub-folders: 
    * `/usr/bin` contains binary files for user programs/commands.
    * `/usr/sbin` contains binary files for system admins.
    * `/usr/lib` contains libraries for `/usr/bin` and `/usr/sbin`.
    * `/usr/local` contains user programs that you install from source. 
    * `/usr/src` holds the Linux kernel sources, header-files, and documentation. 
  
**Example(s):** Some good to know sub-folders are `/usr/local` (someapp config files lie here), `/user/bin` (commands that user installed can be found here).