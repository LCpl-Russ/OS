# Linux Boot Process
## BIG MIKE GOT KILLED IN RUSSSIA 1
- BIOS -Basic Input Output System
- MBR -Master Boot Record
- GRUB -Grand Unified Bootloader
- Kernel 
- Init (SysV or SystemD)
- Run Levels
## BIG MIKE GOT KILLED IN RUSSIA 2
- The machine’s BIOS or boot firmware loads and runs a boot loader.
- The boot loader(“Grub” located in MBR) finds the kernel image on disk, loads it into memory, and starts it.
-  The kernel initializes the devices and its drivers.
- The kernel mounts the root filesystem.
- The kernel starts a program called init with a process ID of 1. This point is the user space start.
- Init sets the rest of the system processes in motion via pre-configured runlevels.
### BIG
Bios - Basic Input Output System
- First program to run on startup (Flash or ROM)
  - If stored in flash memory → becomes a target for BIOS Rootkits
- Perform POST
- system integrity checks
- build a device tree
- reads and executes first secotr on memory
### MIKE
MBR - Master Boot Record
- locate at the beginning of the partition
- contains code for GRUB
- First 512 bytes
### GOT
- GRUB - Grand Unified Bootloader
  - Dynamically configurable with the capability to make changes during boot
    - config file - /boot/grub/menu.lst
    - altering boot entries, selecting different kernels (init.rd)
