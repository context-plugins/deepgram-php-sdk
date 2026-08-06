# Manage V1 Projects Billing Purchases

```php
$manageV1ProjectsBillingPurchasesApi = $client->getManageV1ProjectsBillingPurchasesApi();
```

## Class Name

`ManageV1ProjectsBillingPurchasesApi`


# List

Returns the original purchased amount on an order transaction

```php
function mList(string $projectId, ?float $limit = 10): ApiResponse
```

## Authentication

This endpoint requires [ApiKeyAuth](../../doc/auth/custom-header-signature.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `limit` | `?float` | Query, Optional | Number of results to return per page. Default 10. Range [1,1000]<br><br>**Default**: `10` |

## Response Type

**200**: A list of purchases for a specific project

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ListProjectPurchasesV1Response`](../../doc/models/list-project-purchases-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$limit = 10;

$manageV1ProjectsBillingPurchasesApi = $client->getManageV1ProjectsBillingPurchasesApi();
$apiResponse = $manageV1ProjectsBillingPurchasesApi->mList(
    $projectId,
    $limit
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ListProjectPurchasesV1Response:';
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

