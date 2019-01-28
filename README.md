# disk-partition-units
A units chart for size in disk partitioning and file tools. For those moments when a megabyte is not a mebibyte, Linux or otherwise.

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

### INSTALLER
**Program** | **Unit / Comment**
--- | ---
Ubuntu|GB (assimilates GiB)
Debian|GB (assimilates GiB)
Fedora|GB (GiB in "Settings")
OpenSuse|
Manjaro|
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
* "but also" means the former is used as default but the latter is available as option

### OTHER
**Program** | **Unit / Comment**
--- | ---
df/du/ls|G=1024,GB=1000
swapon|GiB (--show)
dd|GB=1000,G=1024
lsblk|GiB
free|GiB but also GB
* comma-separated values means they are not the default but are available as options
* "but also" means the former is used as default but the latter is available as option
