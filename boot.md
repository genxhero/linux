# The Booting Process

## Step 1: BIOS

BIOS, or basic input output system, is built-in software found on the motherboard.  It scans for devices, such as hard disks and CD Drives, and loads any that it finds.
Then BIOS searches for the Master Boot Record (or, MBR if you would) on the primary hard drive.  
It scans for the 1st stage loader (GRUB LILO for Linux)  and then lets the MBR take over.  

The source from which I am learning Linux gives the following turn of phrase:
"Boot PROM/FLASH/BIOS is proficient of loading the MBR into RAM and executing it."


### The Master Boot Record

