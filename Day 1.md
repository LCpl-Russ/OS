# Day 1 Notes
## Powershell Stuffs
#### Powershell Profiles
##### Powershell Profiles
- Current User, Current Hosts
- Current User, All Host
- All Users, Current Host
- All Users, All Hosts
##### ISE Profiles
- Current User, Current Host
- All Users, Current Host
#### Remoting
##### WSMAN
- get-item WSMAN:\localhost\Client\TrustedHosts
- set-item WSMAN:\localhost\Client\TrustedHosts -value "domain-control"
- set-item WSMAN:\localhost\Client\TrustedHosts -value "file-server,domain-control"
##### Download
- $start_time = get-date
- $wc = New-bject system.net.webclient
- $wc.DownloadFile($url, $ouput)
