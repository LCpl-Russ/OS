# Windows Process Vailidity
How do we discover Normal, abnormal, and Hidden Processes and Services?
```
- Get-Process SMSS,CSRSS,LSASS | Sort -Property Id
```
Do boot processes have descriptions?
```
- Get-Process | Select Name, Id, Description | Sort -Property Id
```
Where do the system processes and services normally run from? (C:\Windows\System32)
```
- Get-Process | Select Name, Id, Path
```
```
- Get-Ciminstance Win32_service | Select Name, Processid, Pathname
```
Are Priority Levels of processes important?
```
- Get-Process | Select Name, Priorityclass
```
```
- Tasklist /m
```
How would malware use Schedule Task?
```
- schtasks /query | more
```
~~~
- Get-ScheduledTask | Select * | Select -First 5
~~~
