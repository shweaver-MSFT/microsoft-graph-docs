---
title: "List governanceRoleDefinitions"
description: "Get a collection of governanceRoleDefinitions on a resource."
localization_priority: Normal
doc_type: apiPageType
author: "davidmu1"
ms.prod: "microsoft-identity-platform"
---

# List governanceRoleDefinitions

Namespace: microsoft.graph
[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a collection of [governanceRoleDefinitions](../resources/governanceroledefinition.md) on your Azure AD roles.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type      | Permissions              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | PrivilegedAccess.ReadWrite.AzureResources  |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | PrivilegedAccess.Read.AzureAD |

Besides the permission scope, this API requires the requestor to have at least one role assignment on the resource.

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedAccess/aadRoles/resources/{resourceId}/roleDefinitions
GET /privilegedAccess/aadRoles/roleDefinitions?$filter=resourceId+eq+'{resourceId}'
```
## Optional query parameters
This method supports the [OData query parameters](/graph/query-parameters) to help customize the response.

## Request headers
| Name      |Description|
|:----------|:----------|
| Authorization  | Bearer {code}|

## Request body
Do not supply a request body for this method.
## Response
If successful, this method returns a `200 OK` response code and collection of [governanceRoleDefinition](../resources/governanceroledefinition.md) objects in the response body.

## Example

<!-- {
  "blockType": "request",
  "name": "get_governanceroledefinitions"
}-->

This example shows how to get all role definitions in the Contoso directory.

### Request

```http
GET https://graph.microsoft.com/beta/privilegedAccess/aadRoles/resources/e5e7d29d-5465-45ac-885f-4716a5ee74b5/roleDefinitions  
```

### Response
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.governanceRoleDefinition",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-Length: 21906

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#governanceRoleDefinitions",
    "value": [
        {
            "id": "00efc9e0-1b96-4e9a-99a3-a3df0735cf88",
            "resourceId": "e5e7d29d-5465-45ac-885f-4716a5ee74b5",
            "externalId": "/subscriptions/befefa01-2a29-4197-83a8-272ff33ce314/providers/Microsoft.Authorization/roleDefinitions/befefa01-2a29-4197-83a8-272ff33ce314",
            "templateId": "befefa01-2a29-4197-83a8-272ff33ce314",
            "displayName": "Global Administrator"
        },
        {
            "id": "051f7264-a992-429a-b345-90415af9f917",
            "resourceId": "e5e7d29d-5465-45ac-885f-4716a5ee74b5",
            "externalId": "/subscriptions/c12c1c16-33a1-487b-954d-41c89c60f349/providers/Microsoft.Authorization/roleDefinitions/c12c1c16-33a1-487b-954d-41c89c60f349",
            "templateId": "c12c1c16-33a1-487b-954d-41c89c60f349",
            "displayName": "Exchange Administrator"
        },
        {
            "id": "0789c03d-445d-40ab-aed3-d110a98146c7",
            "resourceId": "e5e7d29d-5465-45ac-885f-4716a5ee74b5",
            "externalId": "/subscriptions/5d28c62d-5b37-4476-8438-e587778df237/providers/Microsoft.Authorization/roleDefinitions/5d28c62d-5b37-4476-8438-e587778df237",
            "templateId": "5d28c62d-5b37-4476-8438-e587778df237",
            "displayName": "SharePoint Administrator"
        },
  ]
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "List governanceRoleDefinitions",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
