# Confide.Client - the PowerShell module for the Confide API

<a name="frameworks-supported"></a>
## Frameworks supported
- PowerShell 5.1 or later

<a name="installation"></a>
## Installation

To install from PowerShell Gallery (https://www.powershellgallery.com/packages/Confide.Client)
```powershell
Install-Module -Name Confide.Client -Verbose
```
Then import module before executing the PowerShell command
```powershell
Import-Module -Name Confide.Client -Verbose
```
<a name="how-to-use"></a>
## How to use
### 1. [**Connect-Confide**](docs/ConfideConnectApi.md#connect-confide)
To use Confide PowerShell Client, one need to connect to Confide public API with PowerShell:
```powershell
# by Client Secret
Connect-Confide `
    -Url "confide public api url" `
    -ClientId "application client id from AOS" `
    -ClientSecret "your client secret"
```
```powershell
# by Client Certificate
Connect-Confide `
    -Url "confide public api url" `
    -ClientId "application client id from AOS" `
    -Certificate $certificate
```
You can construct the $certificate parameter by the following two ways:
```powershell
# get from .pfx file with the password
$certificate = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2 "path_to_pfx_file", "password"

# get from certificate store of local machine by certificate thumbprint, you need install the certificate to local machine in advance and replace the certificate thumbprint to yours
$certificate = (Get-ChildItem -Path 'Cert:\LocalMachine\My\304CAFB0719971D7F180DE983F649DFAC85D47D3' -Recurse)[0]
```
After you connect to Confide public API, then you can perform various operations like creating projects, adding mappings to projects, running jobs and monitoring mapping migration status, etc.

### 2. [**Add-ConfideShareCenterUserImportTask**](docs/ConfideShareSettingApi.md#add-confidesharecenteruserimporttask)
Imports sharing users from a CSV file and assigns permissions to them in a Confide project. You can find the template for the CSV file in the `templates` folder.

```powershell
# Example: Add users for a specific project
$taskId = Add-ConfideShareCenterUserImportTask -CsvPath "C:\path\to\your\Import_User_Template.csv"
```
This command will return a task ID that you can use to track the import status.

### 3. [**Get-ConfideShareCenterUserImportTask**](docs/ConfideShareSettingApi.md#get-confidesharecenteruserimporttask)
After submitting an import task, you can check its status using the task ID.

```powershell
# Example: Check the status of an import task
Get-ConfideShareCenterUserImportTask -Id $taskId
```
This will return the current status of the user import process.

## Documentation for Cmdlets

For more details on the available cmdlets, please refer to the [**documentation**](docs/ConfideShareSettingApi.md).

## About Confide

[AvePoint Confide](https://www.avepointonlineservices.com) is a virtual data room (VDR) solution that helps organizations share and protect sensitive data with external parties. It provides a secure environment for collaboration, ensuring that confidential information is only accessible to authorized users.
