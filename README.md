# disk-partition-units
A units chart for size in disk partitioning and file tools. For those moments when a megabyte is not a mebibyte, Linux or otherwise.

Have you ever been in that situation where you created a 200 GB partition during an installation and later found that it's actually 186 GiB when using a file manager or other command-line (shell) tools?

* GiB refers to the traditional binary unit (2^n), commonly denoted GB in the past, also known as IEC unit
* GB refers to the newer but confusing decimal unit (10^n), adopted by millennials, also known as SI (ISO) unit

(I've used GiB/GB as an example but all other multiple values are typically available: KiB,MiB,GiB,TiB,PiB,EiB,ZiB,YiB)

### TEXT-BASED
**Program** | **Unit / Comment**
--- | ---
fdisk | G=GiB but also GB (for backward compatibility)
gdisk | GiB
parted | GB
* "but also" means the former is used as default but the latter is available as option

### GRAPHICAL
**Program** | **Unit / Comment**
--- | ---
GParted|GiB
Gnome Disks|GB (buggy, says "free space" for extended)
KDE Partition Manager|GiB

### VIRTUAL / CLOUD
**Program** | **Unit / Comment**
--- | ---
VirtualBox|GiB (shown as GB)
VMware Player|
ec2-create-volume|GiB

### INSTALLER
**Program** | **Unit / Comment**
--- | ---
Ubuntu|GB (assimilates GiB)
Debian|GB (assimilates GiB)
Fedora|GB (GiB in "Settings")
OpenSuse|
Manjaro|
Windows 7|GiB (shown as GB)
Windows 10|
* "assimilates" means the unit is disregarded and the default unit is used instead
* Fedora has a strange unit combination for initial size and for subsequent changes

### FILE MANAGER
**Program** | **Unit / Comment**
--- | ---
Dolphin|GiB
Nemo|GB but also GiB
Krusader|GiB
Nautilus|GB
Double Commander|GiB
Midnight Commander|GB but also GiB
Windows Explorer|GiB (shown as GB)
* "but also" means the former is used as default but the latter is available as option

### OTHER
**Program** | **Unit / Comment**
--- | ---
df/du/ls|GiB,GB (both shown as G)
swapon --show|GiB (shown as G)
dd|GB=1000,G=1024
lsblk|GiB (shown as G)
free|GiB but also GB (both shown without the B)
* comma-separated values means they are not the default but are available as options
* "but also" means the former is used as default but the latter is available as option
