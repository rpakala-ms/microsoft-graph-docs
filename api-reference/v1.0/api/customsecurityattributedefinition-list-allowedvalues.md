---
title: "List allowedValues"
description: "Get a list of the allowedValue objects and their properties."
author: "Cecily"
ms.localizationpriority: medium
ms.prod: "directory-management"
doc_type: apiPageType
---

# List allowedValues

Namespace: microsoft.graph

Get a list of the [allowedValue](../resources/allowedvalue.md) objects and their properties.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|CustomSecAttributeDefinition.Read.All, CustomSecAttributeDefinition.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|CustomSecAttributeDefinition.Read.All, CustomSecAttributeDefinition.ReadWrite.All|

[!INCLUDE [rbac-customsecurityattibutes-apis-definition-assignment-read](../includes/rbac-for-apis/rbac-customsecurityattibutes-apis-definition-assignment-read.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /directory/customSecurityAttributeDefinitions/{customSecurityAttributeDefinitionId}/allowedValues
```

## Optional query parameters

This method supports the `$select` OData query parameter to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [allowedValue](../resources/allowedvalue.md) objects in the response body.

## Examples

### Request

The following example gets all predefined values for a custom security attribute definition.

+ Attribute set: `Engineering`
+ Attribute: `Project`

<!-- {
  "blockType": "request",
  "name": "list_allowedvalue",
  "sampleKeys": ["Engineering_Project"]
}
-->
``` http
GET https://graph.microsoft.com/v1.0/directory/customSecurityAttributeDefinitions/Engineering_Project/allowedValues
```

### Response

The following is an example of the response.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.allowedValue)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#directory/customSecurityAttributeDefinitions('Engineering_Project')/allowedValues",
    "value": [
        {
            "id": "Cascade",
            "isActive": true
        },
        {
            "id": "Baker",
            "isActive": true
        },
        {
            "id": "Alpine",
            "isActive": true
        }
    ]
}
```
