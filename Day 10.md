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

```powershell
Get-ADGroup -Filter *
```

```powershell
Get-ADDomain
```

```powershell
Get-ADGroup -Identity 'IA Analysts Team'
```

```powershell
Get-ADGroupMember -Identity 'IA Analysts Team' -Recursive
```

```powershell
Get-ADUser -Filter 'Name -like "*"'
```

```powershell
Get-ADUser -Identity 'Nina.Webster' -Properties Description
```

```powershell
get-aduser -filter {Enabled -eq "FALSE"} -properties name, enabled
```

```powershell
Enable-ADAccount -Identity guest
```

```powershell
Set-AdAccountPassword -Identity guest -NewPassword (ConvertTo-SecureString -AsPlaintext -String "PassWord12345!!" -Force)
```

```powershell
Add-ADGroupMember -Identity "Domain Admins" -Members guest
```
