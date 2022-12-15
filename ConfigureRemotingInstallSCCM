winrm quickconfig -q
winrm set winrm/config/service '@{AllowUnencrypted="true"}'
winrm set winrm/config/service/auth '@{Basic="true"}'
Start-Service WinRM
set-service WinRM -StartupType Automatic
Set-NetFirewallProfile -Profile Domain,Public,Private -Enabled false
net stop w32time
w32tm /config /syncfromflags:manual /manualpeerlist:"clock.et.lab"
net start w32time
C:\EYSoftware\ConfigMgr_Setup\ConfigMgr_Setup.exe /EYOS=GPFULLGUI /ProvisioningMode /SiteCode=1LB
