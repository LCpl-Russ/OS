# Active Directory
Get a list of AD Commands Available
``` powershell
Get-Command -Module activedirectory
```
Check for any Fine-Grained Password Policies
```powershell
Get-ADFineGrainedPasswordPolicy -Filter {name -like "*"}
```
Get Forest details
```powershell
Get-ADForest
```
Get Domain details:
```powershell
Get-ADGroup -Filter *
```
Get AD Groups
```powershell
Get-ADDomain
```
Get a groups details
```powershell
Get-ADGroup -Identity 'IA Analysts Team'
```
Get a list of a groups members
```powershell
Get-ADGroupMember -Identity 'IA Analysts Team' -Recursive
```
Get AD users
```powershell
Get-ADUser -Filter 'Name -like "*"'
```
To see additional properties, not just the default set
```powershell
Get-ADUser -Identity 'Nina.Webster' -Properties Description
```
Find Disabled users
```powershell
get-aduser -filter {Enabled -eq "FALSE"} -properties name, enabled
```
Enable that user
```powershell
Enable-ADAccount -Identity guest
```
Change the password
```powershell
Set-AdAccountPassword -Identity guest -NewPassword (ConvertTo-SecureString -AsPlaintext -String "PassWord12345!!" -Force)
```
Add the user to an Admin Group
```powershell
Add-ADGroupMember -Identity "Domain Admins" -Members guest
```
