# Windows Boot Process & BCD
## BIOS vs UEFI
- BIOS and UEFI are firmware that ensure critical hardware like SATA devices (Hard Drives), Display Adapters, and SDRAM(Synchronous dynamic random-access memory) are functional then, locates the MBR(Master Boot Record) or GPT(GUID Partition Tables).
### BIOS Master Boot Record
Once the BIOS checks hardware, it finds the MBR (Master Boot Record). The MBR contains Disk Partitions like /dev/sda1 or DISK 1 C:\
The partition contains code that starts the first stage of loading an Operating System, called a Boot Loader
- Boot Loaders
  - Windows 2003 and older used NTLDR or New Technology Loader
  - Windows 7 Service Pack 1 and newer uses bootmgr or New Technology Loader
from this point the Boot Loader takes over and starts the Operating System
### UEFI Boot Manager
UEFI does the same hardware checks as BIOS, but instead of using the MBR it reads an EFI Partition. The EFI Partition contains UEFI Boot Managers
- Windows bootmgfw.efi or Windows Boot Manager
From this point onwards, the UEFI Boot Manager takes over and starts the Operating System
## Windows System Initialization
This is a simplified version of the Windows Boot Process from the kernel (ntoskrnl.exe) to the execution of LogonUi.exe (the process that prompts for user interaction). It is broken into five steps.
1. Loading the Operating System Kernel
2. Initializing the Kernel
2. Starting Subsystems
4. Starting Session 0
9. Starting Session 1
