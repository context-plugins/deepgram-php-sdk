# Manage V1 Projects Usage Fields

```php
$manageV1ProjectsUsageFieldsApi = $client->getManageV1ProjectsUsageFieldsApi();
```

## Class Name

`ManageV1ProjectsUsageFieldsApi`


# List

Lists the features, models, tags, languages, and processing method used for requests in the specified project

:information_source: **Note** This endpoint does not require authentication.

```php
function mList(
    string $projectId,
    string $authorization,
    ?\DateTime $start = null,
    ?\DateTime $end = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |
| `start` | `?DateTime` | Query, Optional | Start date of the requested date range. Format accepted is YYYY-MM-DD |
| `end` | `?DateTime` | Query, Optional | End date of the requested date range. Format accepted is YYYY-MM-DD |

## Response Type

**200**: A list of fields for a specific project

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`UsageFieldsV1Response`](../../doc/models/usage-fields-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$authorization = 'Authorization8';

$manageV1ProjectsUsageFieldsApi = $client->getManageV1ProjectsUsageFieldsApi();
$apiResponse = $manageV1ProjectsUsageFieldsApi->mList(
    $projectId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'UsageFieldsV1Response:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid Request | `ApiException` |

