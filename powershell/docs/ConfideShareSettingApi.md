# Confide.Client\Api.ConfideShareSettingApi


Method | Description
------------- | -------------
[**Add-ConfideShareCenterUserImportTask**](ConfideShareSettingApi.md#add-confidesharecenteruserimporttask) | Import sharing users and assign permissions from a CSV file. | 
[**Get-ConfideShareCenterUserImportTask**](ConfideShareSettingApi.md#get-confidesharecenteruserimporttask) | Get the status of a user import task. | 


<a id="Add-ConfideShareCenterUserImportTask"></a>
# **Add-ConfideShareCenterUserImportTask**
> CloudSdkDataVdrUserExecuteResult Add-ConfideShareCenterUserImportTask<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CsvPath] <String><br>

Import sharing users and assign permissions from a CSV file.

### Example
```powershell
$result = Add-ConfideShareCenterUserImportTask -CsvPath "C:\path\to\your\Import_User_Template.csv"
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Path** | **String**| The file path of the CSV file for importing users. | 

### Return type

**string**



[[Back to top]](#) [[Back to API list]](ConfideApi.md) [[Back to README]](../README.md)

<a id="Get-ConfideShareCenterUserImportTask"></a>
# **Get-ConfideShareCenterUserImportTask**
> CloudSdkDataVdrImportStatus Get-ConfideShareCenterUserImportTask<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>

Get the status of a user import task.

### Example
```powershell
$status = Get-ConfideShareCenterUserImportTask -Id "your_task_id"
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**| The Id of the import task. | 


### Return type

[**ImportUserResponseModel**](ImportUserResponseModel.md) (PSCustomObject)


[[Back to top]](#) [[Back to API list]](ConfideApi.md) [[Back to README]](../README.md)
