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
