﻿# assign action

> **Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change. Use of these APIs in production applications is not supported.

> **Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.

Not yet documented
## Prerequisites
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).

|Permission type|Permissions (from most to least privileged)|
|:---|:---|
|Delegated (work or school account)|DeviceManagementApps.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|Not supported.|

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks/{managedEBookId}/assign
POST /deviceAppManagement/managedEBooks/{managedEBookId}/groupAssignments/{eBookGroupAssignmentId}/eBook/assign
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
In the request body, supply JSON representation of the parameters.

The following table shows the parameters that can be used with this action.

|Property|Type|Description|
|:---|:---|:---|
|eBookGroupAssignments|[eBookGroupAssignment](../resources/intune_books_ebookgroupassignment.md) collection|Not yet documented|
|managedEBookAssignments|[managedEBookAssignment](../resources/intune_books_managedebookassignment.md) collection|Not yet documented|



## Response
If successful, this action returns a `204 No Content` response code.

## Example
### Request
Here is an example of the request.
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/managedEBooks/{managedEBookId}/assign

Content-type: application/json
Content-length: 568

{
  "eBookGroupAssignments": [
    {
      "@odata.type": "#microsoft.graph.eBookGroupAssignment",
      "targetGroupId": "Target Group Id value",
      "id": "6cb57cb9-7cb9-6cb5-b97c-b56cb97cb56c",
      "installIntent": "required"
    }
  ],
  "managedEBookAssignments": [
    {
      "@odata.type": "#microsoft.graph.managedEBookAssignment",
      "id": "ae8b0d27-0d27-ae8b-270d-8bae270d8bae",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      },
      "installIntent": "required"
    }
  ]
}
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 204 No Content
```



