# The Booting Process

## Step 1: BIOS

BIOS, or basic input output system, is built-in software found on the motherboard.  It scans for devices, such as hard disks and CD Drives, and loads any that it finds.
Then BIOS searches for the Master Boot Record (or, MBR if you would) on the primary hard drive.  
It scans for the 1st stage loader (GRUB LILO for Linux)  and then lets the MBR take over.  