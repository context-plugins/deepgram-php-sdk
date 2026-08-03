# Manage V1 Projects Billing Balances

```php
$manageV1ProjectsBillingBalancesApi = $client->getManageV1ProjectsBillingBalancesApi();
```

## Class Name

`ManageV1ProjectsBillingBalancesApi`

## Methods

* [List](../../doc/controllers/manage-v1-projects-billing-balances.md#list)
* [Get](../../doc/controllers/manage-v1-projects-billing-balances.md#get)


# List

Generates a list of outstanding balances for the specified project

:information_source: **Note** This endpoint does not require authentication.

```php
function mList(string $projectId, string $authorization): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |

## Response Type

**200**: A list of outstanding balances

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ListProjectBalancesV1Response`](../../doc/models/list-project-balances-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$authorization = 'Authorization8';

$manageV1ProjectsBillingBalancesApi = $client->getManageV1ProjectsBillingBalancesApi();
$apiResponse = $manageV1ProjectsBillingBalancesApi->mList(
    $projectId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ListProjectBalancesV1Response:';
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


# Get

Retrieves details about the specified balance

:information_source: **Note** This endpoint does not require authentication.

```php
function get(string $projectId, string $balanceId, string $authorization): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `balanceId` | `string` | Template, Required | The unique identifier of the balance |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |

## Response Type

**200**: A specific balance

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`GetProjectBalanceV1Response`](../../doc/models/get-project-balance-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$balanceId = 'balance_id2';

$authorization = 'Authorization8';

$manageV1ProjectsBillingBalancesApi = $client->getManageV1ProjectsBillingBalancesApi();
$apiResponse = $manageV1ProjectsBillingBalancesApi->get(
    $projectId,
    $balanceId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'GetProjectBalanceV1Response:';
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

