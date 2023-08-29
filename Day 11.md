# https://os.cybbh.io/public/os/latest/index.html
# Final Review
##### Persistence
###### powershell profiles
- run every single time
- runs in order
###### ports in windows
- netstat -ano
- suspicious ports use weird patterns
    - 4444, 9999, 1234
###### ports in Linux
- sudo netstat -ano/anop
- 
###### Processses
- get-process
- autoruns
- taskmanager
- ps -elf
- top / htop
- suspicious
    - non-standard location
    - misspelled name
###### Services
###### Scheduled tasks
- Schtasks
- get-ScheduledTask
###### Registry
- AutoRuns
- Regedit
    - hkey_local_machine
    - hkey_users
    - hkey_currentUser

