# Active Directory
Get a list of AD Commands Available
'''
Get-Command -Module activedirectory
'''
Get-ADFineGrainedPasswordPolicy -Filter {name -like "*"}

Get-ADForest
Get-ADGroup -Filter *
Get-ADDomain
Get-ADGroup -Identity 'IA Analysts Team'
Get-ADGroupMember -Identity 'IA Analysts Team' -Recursive
Get-ADUser -Filter 'Name -like "*"'
Get-ADUser -Identity 'Nina.Webster' -Properties Description
get-aduser -filter {Enabled -eq "FALSE"} -properties name, enabled
Enable-ADAccount -Identity guest
Set-AdAccountPassword -Identity guest -NewPassword (ConvertTo-SecureString -AsPlaintext -String "PassWord12345!!" -Force)
Add-ADGroupMember -Identity "Domain Admins" -Members guest
