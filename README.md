A units chart for size in disk partitioning and file tools. For those moments when a megabyte is not a mebibyte, Linux or otherwise.

Have you ever been in that situation where you created a 200 GB partition during an installation and later found that it's actually 186 GiB when using a file manager or other command-line (shell) tools? Here's a time saving cheatsheet that will save you from a lot of trial and error.

* GiB refers to the traditional binary unit (2ⁿ or 1024), commonly denoted GB in the past, also known as IEC prefix
* GB refers to the newer but confusing decimal unit (10ⁿ or 1000), embraced by millennials, also known as SI (ISO) prefix

(I've used GiB/GB as an example but all other multiple values are typically also available: KiB,MiB,GiB,TiB,PiB,EiB,ZiB,YiB)

### TEXT-BASED
**Program** | **Unit / Comment**
--- | ---
fdisk | G=GiB but also GB (for backward compatibility)
gdisk | GiB
cfdisk | GiB
cgdisk | GiB
parted | GB
* "but also" means the former is used as default but the latter is available as option

### GRAPHICAL
**Program** | **Unit / Comment**
--- | ---
GParted | GiB
Gnome Disks | GB (buggy, says "free space" for extended)
KDE Partition Manager | GiB

### VIRTUAL / CLOUD
**Program** | **Unit / Comment**
--- | ---
LVM (pv/vg/lv) | GiB
VirtualBox | GiB (labeled GB)
VMware Player | 
ec2-create-volume | GiB

### INSTALLER
**Program** | **Unit / Comment**
--- | ---
Ubuntu | GB (assimilates GiB)
Debian | GB (assimilates GiB)
Fedora | GB (GiB in "Settings")
openSUSE | GiB
Manjaro | (depends on tool chosen)
Windows 7 | GiB (labeled GB)
Windows 10 | GiB (labeled GB)
* "assimilates" means the unit is disregarded and the default unit is used instead
* Fedora has a strange unit combination for initial size and for subsequent changes

### FILE MANAGER
**Program** | **Unit / Comment**
--- | ---
Dolphin | GiB
Nemo | GB but also GiB
Krusader | GiB
Nautilus | GB
Double Commander | GiB (labeled G / custom labels)
Midnight Commander | GB but also GiB
Windows Explorer | GiB (labeled GB)
* "but also" means the former is used as default but the latter is available as option

### SYSTEM INFO
**Program** | **Unit / Comment**
--- | ---
Gnome System Monitor | GB
df | GiB,GB (both labeled G)
swapon --show | GiB (labeled G)
lsblk | GiB (labeled G)
free | GiB but also GB (both labeled without the B)
* comma-separated values means they are not the default but are available as options
* "but also" means the former is used as default but the latter is available as option

### OTHER
**Program** | **Unit / Comment**
--- | ---
du | GiB,GB (both labeled G)
ls | GiB,GB (both labeled G)
dd | GB=1000,G=1024
* comma-separated values means they are not the default but are available as options
