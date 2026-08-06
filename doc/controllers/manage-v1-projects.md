# Manage V1 Projects

```php
$manageV1ProjectsApi = $client->getManageV1ProjectsApi();
```

## Class Name

`ManageV1ProjectsApi`

## Methods

* [List](../../doc/controllers/manage-v1-projects.md#list)
* [Get](../../doc/controllers/manage-v1-projects.md#get)
* [Update](../../doc/controllers/manage-v1-projects.md#update)
* [Delete](../../doc/controllers/manage-v1-projects.md#delete)
* [Leave](../../doc/controllers/manage-v1-projects.md#leave)


# List

Retrieves basic information about the projects associated with the API key

```php
function mList(): ApiResponse
```

## Authentication

This endpoint requires [ApiKeyAuth](../../doc/auth/custom-header-signature.md)

## Response Type

**200**: A list of projects

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ListProjectsV1Response`](../../doc/models/list-projects-v1-response.md).

## Example Usage

```php
$manageV1ProjectsApi = $client->getManageV1ProjectsApi();
$apiResponse = $manageV1ProjectsApi->mList();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ListProjectsV1Response:';
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

Retrieves information about the specified project

```php
function get(string $projectId, ?float $limit = 10, ?float $page = null): ApiResponse
```

## Authentication

This endpoint requires [ApiKeyAuth](../../doc/auth/custom-header-signature.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `limit` | `?float` | Query, Optional | Number of results to return per page. Default 10. Range [1,1000]<br><br>**Default**: `10` |
| `page` | `?float` | Query, Optional | Navigate and return the results to retrieve specific portions of information of the response |

## Response Type

**200**: A project

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`GetProjectV1Response`](../../doc/models/get-project-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$limit = 10;

$manageV1ProjectsApi = $client->getManageV1ProjectsApi();
$apiResponse = $manageV1ProjectsApi->get(
    $projectId,
    $limit
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'GetProjectV1Response:';
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


# Update

Updates the name or other properties of an existing project

```php
function update(string $projectId, ?UpdateProjectV1Request $body = null): ApiResponse
```

## Authentication

This endpoint requires [ApiKeyAuth](../../doc/auth/custom-header-signature.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `body` | [`?UpdateProjectV1Request`](../../doc/models/update-project-v1-request.md) | Body, Optional | The name of the project |

## Response Type

**200**: A project

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`UpdateProjectV1Response`](../../doc/models/update-project-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$manageV1ProjectsApi = $client->getManageV1ProjectsApi();
$apiResponse = $manageV1ProjectsApi->update($projectId);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'UpdateProjectV1Response:';
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


# Delete

Deletes the specified project

```php
function delete(string $projectId): ApiResponse
```

## Authentication

This endpoint requires [ApiKeyAuth](../../doc/auth/custom-header-signature.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |

## Response Type

**200**: A project

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`DeleteProjectV1Response`](../../doc/models/delete-project-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$manageV1ProjectsApi = $client->getManageV1ProjectsApi();
$apiResponse = $manageV1ProjectsApi->delete($projectId);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'DeleteProjectV1Response:';
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


# Leave

Removes the authenticated account from the specific project

```php
function leave(string $projectId): ApiResponse
```

## Authentication

This endpoint requires [ApiKeyAuth](../../doc/auth/custom-header-signature.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |

## Response Type

**200**: Successfully removed account from project

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`LeaveProjectV1Response`](../../doc/models/leave-project-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$manageV1ProjectsApi = $client->getManageV1ProjectsApi();
$apiResponse = $manageV1ProjectsApi->leave($projectId);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'LeaveProjectV1Response:';
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

