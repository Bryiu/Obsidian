# How to extend the LVM
Command | Description
------------ | ------------
cfdisk /dev/sda | create new partition, using all free space
pvcreate /dev/sdaX | initialize partition for use with LVM
vgdisplay | to find VG name
vgextend /dev/vgname /dev/sdaX | this extends the volume group
lvextend -l +100%FREE /dev/vgname/root | this extends the LVM
resize2fs /dev/vgname/root  | this extends the filesystem

# Explanation of LVM

LVM doesn't care about partitions. A LVM has the following hierachy:

1.  Filesystem
2.  **L**ogical **V**olumes
3.  **V**olume **G**roups
4.  **P**hysical **V**olumes
5.  (Partitions)
6.  Hardware

Lets go from the bottom up.

At the bottom you have the hardware. Big surprise. On top of that you have PVs. Now here is where it becomes confusing. You can either have a PV be the drive itself _or a partition_. LVM does not need partitions. You can add raw block devices as PVs. However, many people create partitions anyways. There are many reasons for this. Backwards compatibility with tools or people that expect partitions, for example. If a sysadmin does not know the layout and sees an 'empty' disk, he might think the disk is empty, although it is a PV! So thats the reason why you sometimes use partitions as PVs.

This is what you see in your example, whoever set the server up created one partition per VG, apparently.

Next up are the volume groups. A VG is one or multiple PVs. This is the container that holds all the stuff that comes afterwards. Since PVs can be disks, virtual disks from RAID controllers, partitions, etc., VGs can span any number of these things.

On top of VGs you have LVs. This is what you actually put your filesystems on top of. You can look at a LV kind of like a partition. You can find them here:

```
/dev/VGName/LVname
```

So a LV always belongs to one VG, but you can have many LVs per VG.

On top of the LV, finally, you put your filesystem.

# Why loop

The loop conundrum: there is no loop device! Parted cannot find a partition table on the LVM (as it should be), so it just displays 'loop' instead.