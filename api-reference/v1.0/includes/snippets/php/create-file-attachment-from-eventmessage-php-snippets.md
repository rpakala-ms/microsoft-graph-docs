---
description: "Automatically generated file. DO NOT MODIFY"
---

```php

<?php

// THIS SNIPPET IS A PREVIEW FOR THE KIOTA BASED SDK. NON-PRODUCTION USE ONLY
$graphServiceClient = new GraphServiceClient($requestAdapter);

$requestBody = new Attachment();
$requestBody->set@odatatype('microsoft.graph.fileAttachment');

$requestBody->setName('name-value');

$requestBody->setContentType('contentType-value');

$requestBody->setIsInline(false);

$additionalData = [
		'contentLocation' => 'contentLocation-value', 
		'contentBytes' => 'base64-contentBytes-value', 
];
$requestBody->setAdditionalData($additionalData);




$result = $graphServiceClient->me()->messages()->byMessageId('message-id')->attachments()->post($requestBody);


```