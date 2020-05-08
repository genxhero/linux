# The Booting Process

## BIOS

BIOS, or basic input output system, is built-in software found on the motherboard.  It scans for devices, such as hard disks and CD Drives, and loads any that it finds.
Then BIOS searches for the Master Boot Record (or, MBR if you would) on the primary hard drive.  
It scans for the 1st stage loader (GRUB LILO for Linux)  and then lets the MBR take over.  

The source from which I am learning Linux gives the following turn of phrase:
"Boot PROM/FLASH/BIOS is proficient of loading the MBR into RAM and executing it."
I am as of this commit still having trouble parsing it.
TODO: Figure out what "proficient **of**" even means.  Is this an oversight by the

## The Master Boot Record

The MBR is about 512 bytes of space. It contains information neccesary to loading most operating systems and also the binary information of the 1st stage loader.  The MBR is a physical sector of the first disk drive and isn't a part of any particular partition.  This physical location is in the prime sector of the first cylinder (track 0, head 0). The MBR uses mini executable programs and a table to specify primary partitions.  Additionally, the MBR keeps track of which primary partition is active.  The BIOS lets the first stage boot loader take over, which then proceeds to scan the partition table for the second stage boot loader on the bootable partition

## Boot Loader

Once the stage 2 boot loader (GRUB or LILO) is loaded into RAM it searches for the Kernel inside of the map file and loads it.  That is to say that GRUB loads the kernel from the /boot partitiion.