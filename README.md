
libparted/disk.c writes:
 <i>Most programs will need to use ped_disk_new() or ped_disk_new_fresh() to get
 anything done.<br>
 A PedDisk is always associated with a device and has a
 partition table.  There are different types of partition tables (or disk
 labels).  These are represented by the PedDiskType enumeration.</i>

**`PedDevice`** represents a block device (such as `/dev/hd*`, `/dev/sd*` and is defined in `include/parted/device.h`.

**`PedDeviceType`** is an enum that represents SCSI, IDE etc. It is defined in `include/parted/device.h`.

**`PedDisk`**: represents a partition table (aka disk label) (`include/parted/disk.h`).

**`PedPartition`** represents a partition (`include/parted/disk.h`).

**`PedDiskType`** is defined in `include/parted/disk.h`. It seems as though it represents a partition (but see also `PedPartition`).
`PedDiskTypeFeature` is a bitmap of supported features, such as PED_DISK_TYPE_EXTENDED, PED_DISK_TYPE_PARTITION_NAME etc.

**`PedGeometry`** defines a geometry (that is: start sector, length (or count?) of sectors and end sector) and is defined in `include/parted/geom.h`.

MBR/dos related things seem to be stored under libparted/labels/dos.c
