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
##### PSSession
- $session = New-PSSession -ComputerName file-server -credential andy.dwyer
# Stack Number 10
# IP 10.50.25.206
### xfreerdp /u:andy.dwyer /v:10.50.25.206 /dynamic-resolution +glyph-cache +clipboard
