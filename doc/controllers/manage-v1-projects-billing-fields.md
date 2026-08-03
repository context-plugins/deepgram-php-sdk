# Manage V1 Projects Billing Fields

```php
$manageV1ProjectsBillingFieldsApi = $client->getManageV1ProjectsBillingFieldsApi();
```

## Class Name

`ManageV1ProjectsBillingFieldsApi`


# List

Lists the accessors, deployment types, tags, and line items used for billing data in the specified time period. Use this endpoint if you want to filter your results from the Billing Breakdown endpoint and want to know what filters are available.

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

**200**: A list of billing fields for a specific project

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ListBillingFieldsV1Response`](../../doc/models/list-billing-fields-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$authorization = 'Authorization8';

$manageV1ProjectsBillingFieldsApi = $client->getManageV1ProjectsBillingFieldsApi();
$apiResponse = $manageV1ProjectsBillingFieldsApi->mList(
    $projectId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ListBillingFieldsV1Response:';
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

