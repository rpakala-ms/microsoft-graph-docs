---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-sdk-go/models"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphmodels.NewWorkbookTable()
name := "name-value"
requestBody.SetName(&name) 
showHeaders := true
requestBody.SetShowHeaders(&showHeaders) 
showTotals := true
requestBody.SetShowTotals(&showTotals) 
style := "style-value"
requestBody.SetStyle(&style) 

result, err := graphClient.Drives().ByDriveId("drive-id").Items().ByItemId("driveItem-id").Workbook().Tables().ByTableId("workbookTable-id").Patch(context.Background(), requestBody, nil)


```