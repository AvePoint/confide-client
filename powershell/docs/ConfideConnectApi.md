# Confide.Client\Api.ConfideConnectApi

Method | Description
------------- | -------------
[**Connect-Confide**](ConfideConnectApi.md#connect-confide) | Connect to Confide Public API with Client Credentials/Client Secret.
[**Disconnect-Confide**](ConfideConnectApi.md#disconnect-confide) | Disconnect from Confide Public API.


<a name="Connect-Confide"></a>
# **Connect-Confide**
> Connect-Confide<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Url] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ClientId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ClientSecret] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Certificate] <X509Certificate2><br>

Connect to Confide Public API with Client Credentials/Client Secret.


### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Url** | **String**| The public API URL varies with your data center, you can find it in Confide user guide. 
 **ClientId** | **String**| The application (client) ID you have retrieved from AvePoint Online Service App registrations. 
 **ClientSecret** | **String**| The corresponding client secret you used while registering the AvePoint app. 
 **Certificate** | **X509Certificate2**| The corresponding .pfx certificate file of the .cer certificate you used while registering the AvePoint app. 


### Example
```powershell

$Url = "https://graph-public.sharepointguild.com/confide" 
$ClientId = "4aeeb44e-325a-4002-a36d-2986b65cad0a" 
$ClientSecret = "your client secret" 
$Cert = (Get-ChildItem -Path 'Cert:\LocalMachine\My\304CAFB0719971D7F180DE983F649DFAC85D47D3' -Recurse)[0] 

# Connect with Client Secret
Connect-Confide -Url Url -ClientId $ClientId -ClientSecret $ClientSecret 

# Connect with Certificate
Connect-Confide -Url $Url -ClientId $ClientId -Certificate $Cert
```

[[Back to top]](#) [[Back to API list]](ConfideApi.md) [[Back to README]](../README.md)

<a id="Disconnect-Confide"></a>
# **Disconnect-Confide**
> Disconnect-Confide<br>

Disconnect from Confide API.

### Example
```powershell
Disconnect-Confide
```

[[Back to top]](#) [[Back to API list]](ConfideApi.md) [[Back to README]](../README.md)