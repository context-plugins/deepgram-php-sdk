# Manage V1 Projects Requests

```php
$manageV1ProjectsRequestsApi = $client->getManageV1ProjectsRequestsApi();
```

## Class Name

`ManageV1ProjectsRequestsApi`

## Methods

* [List](../../doc/controllers/manage-v1-projects-requests.md#list)
* [Get](../../doc/controllers/manage-v1-projects-requests.md#get)


# List

Generates a list of requests for a specific project

```php
function mList(
    string $projectId,
    ?\DateTime $start = null,
    ?\DateTime $end = null,
    ?float $limit = 10,
    ?float $page = null,
    ?string $accessor = null,
    ?string $requestId = null,
    ?string $deployment = null,
    ?string $endpoint = null,
    ?string $method = null,
    ?string $status = null
): ApiResponse
```

## Authentication

This endpoint requires [ApiKeyAuth](../../doc/auth/custom-header-signature.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `start` | `?DateTime` | Query, Optional | Start date of the requested date range. Formats accepted are YYYY-MM-DD, YYYY-MM-DDTHH:MM:SS, or YYYY-MM-DDTHH:MM:SS+HH:MM |
| `end` | `?DateTime` | Query, Optional | End date of the requested date range. Formats accepted are YYYY-MM-DD, YYYY-MM-DDTHH:MM:SS, or YYYY-MM-DDTHH:MM:SS+HH:MM |
| `limit` | `?float` | Query, Optional | Number of results to return per page. Default 10. Range [1,1000]<br><br>**Default**: `10` |
| `page` | `?float` | Query, Optional | Navigate and return the results to retrieve specific portions of information of the response |
| `accessor` | `?string` | Query, Optional | Filter for requests where a specific accessor was used |
| `requestId` | `?string` | Query, Optional | Filter for a specific request id |
| `deployment` | [`?string(V1ProjectsProjectIdRequestsGetParametersDeployment)`](../../doc/models/v1-projects-project-id-requests-get-parameters-deployment.md) | Query, Optional | Filter for requests where a specific deployment was used |
| `endpoint` | [`?string(V1ProjectsProjectIdRequestsGetParametersEndpoint)`](../../doc/models/v1-projects-project-id-requests-get-parameters-endpoint.md) | Query, Optional | Filter for requests where a specific endpoint was used |
| `method` | [`?string(V1ProjectsProjectIdRequestsGetParametersMethod)`](../../doc/models/v1-projects-project-id-requests-get-parameters-method.md) | Query, Optional | Filter for requests where a specific method was used |
| `status` | [`?string(V1ProjectsProjectIdRequestsGetParametersStatus)`](../../doc/models/v1-projects-project-id-requests-get-parameters-status.md) | Query, Optional | Filter for requests that succeeded (status code < 300) or failed (status code >=400) |

## Response Type

**200**: A list of requests for a specific project

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ListProjectRequestsV1Response`](../../doc/models/list-project-requests-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$limit = 10;

$manageV1ProjectsRequestsApi = $client->getManageV1ProjectsRequestsApi();
$apiResponse = $manageV1ProjectsRequestsApi->mList(
    $projectId,
    null,
    null,
    $limit
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ListProjectRequestsV1Response:';
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

Retrieves a specific request for a specific project

```php
function get(string $projectId, string $requestId): ApiResponse
```

## Authentication

This endpoint requires [ApiKeyAuth](../../doc/auth/custom-header-signature.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `requestId` | `string` | Template, Required | The unique identifier of the request |

## Response Type

**200**: A specific request for a specific project

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`GetProjectRequestV1Response`](../../doc/models/get-project-request-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$requestId = 'request_id8';

$manageV1ProjectsRequestsApi = $client->getManageV1ProjectsRequestsApi();
$apiResponse = $manageV1ProjectsRequestsApi->get(
    $projectId,
    $requestId
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'GetProjectRequestV1Response:';
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

