# UEditPS
PowerShell settings for UltraEdit (v23+).

## markdown.uew
This is a basic wordfile for the Markdown syntax. 
From the UltraEdit forum post [Markdown Wordfile and preview] (https://www.ultraedit.com/forums/viewtopic.php?f=9&t=13807&p=47901&hilit=markdown+wordfile#p47901) by Mofi.

## powershell.uew
This is the basic PowerShell wordfile available from the UltraEdit site. Modified with the command list from my PowerShell autocomplete file.

## UEdit_PS_Autocomplete.txt
Contains the unique commands from the PowerShell modules installed on my system.

I used PowerShell to get a list of all the modules and they commands for each.
```PowerShell
Get-Module -ListAvailable | select Name | Sort-Object -Property Name
$moduleList = Get-Module -ListAvailable | % {Get-Command -Module $_.Name | select Name}
```

Excel 2016 was used to sort $moduleList and remove duplicates.

The full list of modules follows below.
### PowerShell module list
* AADRM
* AppBackgroundTask
* AppLocker
* Appx
* AssignedAccess
* Azure
* Azure.Storage
* AzureRM.ApiManagement
* AzureRM.Automation
* AzureRM.Backup
* AzureRM.Batch
* AzureRM.Compute
* AzureRM.DataFactories
* AzureRM.DataLakeAnalytics
* AzureRM.DataLakeStore
* AzureRM.Dns
* AzureRM.HDInsight
* AzureRM.Insights
* AzureRM.KeyVault
* AzureRM.Network
* AzureRM.OperationalInsights
* AzureRM.Profile
* AzureRM.RedisCache
* AzureRM.Resources
* AzureRM.SiteRecovery
* AzureRM.Sql
* AzureRM.Storage
* AzureRM.StreamAnalytics
* AzureRM.Tags
* AzureRM.TrafficManager
* AzureRM.UsageAggregates
* AzureRM.Websites
* BitLocker
* BitsTransfer
* BranchCache
* CimCmdlets
* Defender
* DirectAccessClientComponents
* Dism
* DnsClient
* EventTracingManagement
* Exchange Online (from an imported session module)
* International
* iSCSI
* ISE
* Kds
* Microsoft.Online.SharePoint.PowerShell
* Microsoft.PowerShell.Archive
* Microsoft.PowerShell.Diagnostics
* Microsoft.PowerShell.Host
* Microsoft.PowerShell.Management
* Microsoft.PowerShell.ODataUtils
* Microsoft.PowerShell.Security
* Microsoft.PowerShell.Utility
* Microsoft.WSMan.Management
* MMAgent
* MsDtc
* MSOnline
* MSOnlineExtended
* NetAdapter
* NetConnection
* NetEventPacketCapture
* NetLbfo
* NetNat
* NetQos
* NetSecurity
* NetSwitchTeam
* NetTCPIP
* NetworkConnectivityStatus
* NetworkSwitchManager
* NetworkTransition
* PackageManagement
* PackageManagement
* PcsvDevice
* Pester
* PKI
* PnpDevice
* PowerShellGet
* PrintManagement
* PSDesiredStateConfiguration
* PSDiagnostics
* PSFTP
* PSReadline
* PSScheduledJob
* PSWindowsUpdate
* PSWorkflow
* PSWorkflowUtility
* ScheduledTasks
* SecureBoot
* SmbShare
* SmbWitness
* StartLayout
* Storage
* TLS
* TroubleshootingPack
* TrustedPlatformModule
* VpnClient
* Wdac
* WindowsDeveloperLicense
* WindowsErrorReporting
* WindowsSearch
* WindowsUpdate

# Using these files
## Wordfiles
Place the wordfiles (* .uew) in the %appdata%\IDMComp\UltraEdit\wordfiles directory. 
UltraEdit must be restarted to pick up the new/changed wordfiles.

## Autocomplete
I did the following steps to add the PowerShell autocomplete file.

1. Open the UltraEdit settings dialog.
2. Go to Word Wrap/Tab Settings under the Editor section.
  - ![Screenshot 1] (https://github.com/SLight01/UEditPS/blob/master/Images/UE_PS01.png)
3. Add a list for PowerShell file extensions.
  - Select the change list button.
  - Enter the space delimited list of extensions and press Add.
  - ![Screenshot 2] (https://github.com/SLight01/UEditPS/blob/master/Images/UE_PS02.png)
4. In the select extension dropdown choose the new PowerShell extensions item.
  - ![Screenshot 3] (https://github.com/SLight01/UEditPS/blob/master/Images/UE_PS02.png)
5. Browse to the autocomplete file.
