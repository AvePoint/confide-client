# Confide.Client\Api.ConfideShareSettingApi


Method | Description
------------- | -------------
[**Add-ConfideShareCenterUserImportTask**](ConfideShareSettingApi.md#add-confidesharecenteruserimporttask) | Import sharing users and assign permissions from a CSV file. | 
[**Get-ConfideShareCenterUserImportTask**](ConfideShareSettingApi.md#get-confidesharecenteruserimporttask) | Get the status of a user import task. | 
[**Add-ConfideShareCenterUserUpdateTask**](ConfideShareSettingApi.md#add-confidesharecenteruserupdatetask) | Update sharing users permissions from a CSV file. | 
[**Get-ConfideShareCenterUserUpdateTask**](ConfideShareSettingApi.md#get-confidesharecenteruserupdatetask) | Get the status of a user update task. | 

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


<a id="Add-ConfideShareCenterUserUpdateTask"></a>
# **Add-ConfideShareCenterUserUpdateTask**
> CloudSdkDataVdrUserExecuteResult Add-ConfideShareCenterUserUpdateTask<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CsvPath] <String><br>

Update sharing users' permissions from a CSV file.

### Example
```powershell
$result = Add-ConfideShareCenterUserUpdateTask -CsvPath "C:\path\to\your\Update_User_Template.csv"
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Path** | **String**| The file path of the CSV file for updating sharing user permissions. | 

### Return type

**string**



[[Back to top]](#) [[Back to API list]](ConfideApi.md) [[Back to README]](../README.md)

<a id="Get-ConfideShareCenterUserUpdateTask"></a>
# **Get-ConfideShareCenterUserUpdateTask**
> CloudSdkDataVdrUpdateStatus Get-ConfideShareCenterUserUpdateTask<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>

Get the status of a user update task.

### Example
```powershell
$status = Get-ConfideShareCenterUserUpdateTask -Id "your_task_id"
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**| The Id of the update task. | 


### Return type

[**ImportUserResponseModel**](ImportUserResponseModel.md) (PSCustomObject)


[[Back to top]](#) [[Back to API list]](ConfideApi.md) [[Back to README]](../README.md)