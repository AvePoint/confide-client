# ImportUserResponseModel
## Properties
| Property           | Type    | Description |
|--------------------|---------|-------------|
| taskId           | string (uuid)  | The unique identifier for the task. |
| status         | string | The current status of the task. |
| totalCount     | integer | The total number of users in the import task. |
| processedCount  | integer | The number of users that have been processed. |
| failedCount      | integer | The number of users that failed to import. |
| items     | array of ImportUserStatusItem | An array of objects detailing the status for each user. |
| message          | string | A general message about the task status. |
| startTime          | string (date-time) | The time the task started. |
| finishTime        | string (date-time) | The time the task finished. |

[[Back to API list]](ConfideApi.md#documentation-for-cmdlets) [[Back to README]](../README.md)

#### ImportUserStatusItem Properties 

| Property         | Type    | Description |
|------------------|---------|-------------|
| email           | string  | The email address of the user. |
| success     | boolean  | Indicates if the user was imported successfully. |
| status           | string | The import status for the specific user. |
| errorMessage     | string  | Any error message associated with the user's import failure. |

[[Back to API list]](ConfideApi.md#documentation-for-cmdlets) [[Back to README]](../README.md)