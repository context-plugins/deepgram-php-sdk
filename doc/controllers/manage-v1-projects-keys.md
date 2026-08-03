# Manage V1 Projects Keys

```php
$manageV1ProjectsKeysApi = $client->getManageV1ProjectsKeysApi();
```

## Class Name

`ManageV1ProjectsKeysApi`

## Methods

* [List](../../doc/controllers/manage-v1-projects-keys.md#list)
* [Create](../../doc/controllers/manage-v1-projects-keys.md#create)
* [Get](../../doc/controllers/manage-v1-projects-keys.md#get)
* [Delete](../../doc/controllers/manage-v1-projects-keys.md#delete)


# List

Retrieves all API keys associated with the specified project

:information_source: **Note** This endpoint does not require authentication.

```php
function mList(string $projectId, string $authorization, ?string $status = null): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |
| `status` | [`?string(V1ProjectsProjectIdKeysGetParametersStatus)`](../../doc/models/v1-projects-project-id-keys-get-parameters-status.md) | Query, Optional | Only return keys with a specific status |

## Response Type

**200**: A list of API keys

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ListProjectKeysV1Response`](../../doc/models/list-project-keys-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$authorization = 'Authorization8';

$manageV1ProjectsKeysApi = $client->getManageV1ProjectsKeysApi();
$apiResponse = $manageV1ProjectsKeysApi->mList(
    $projectId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ListProjectKeysV1Response:';
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


# Create

Creates a new API key with specified settings for the project

:information_source: **Note** This endpoint does not require authentication.

```php
function create(string $projectId, string $authorization, ?array $body = null): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |
| `body` | array\|null | Body, Optional | API key settings |

## Response Type

**200**: API key created successfully

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`CreateKeyV1Response`](../../doc/models/create-key-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$authorization = 'Authorization8';

$manageV1ProjectsKeysApi = $client->getManageV1ProjectsKeysApi();
$apiResponse = $manageV1ProjectsKeysApi->create(
    $projectId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'CreateKeyV1Response:';
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

Retrieves information about a specified API key

:information_source: **Note** This endpoint does not require authentication.

```php
function get(string $projectId, string $keyId, string $authorization): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `keyId` | `string` | Template, Required | The unique identifier of the API key |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |

## Response Type

**200**: A specific API key

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`GetProjectKeyV1Response`](../../doc/models/get-project-key-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$keyId = 'key_id4';

$authorization = 'Authorization8';

$manageV1ProjectsKeysApi = $client->getManageV1ProjectsKeysApi();
$apiResponse = $manageV1ProjectsKeysApi->get(
    $projectId,
    $keyId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'GetProjectKeyV1Response:';
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

Deletes an API key for a specific project

:information_source: **Note** This endpoint does not require authentication.

```php
function delete(string $projectId, string $keyId, string $authorization): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `keyId` | `string` | Template, Required | The unique identifier of the API key |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |

## Response Type

**200**: API key deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`DeleteProjectKeyV1Response`](../../doc/models/delete-project-key-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$keyId = 'key_id4';

$authorization = 'Authorization8';

$manageV1ProjectsKeysApi = $client->getManageV1ProjectsKeysApi();
$apiResponse = $manageV1ProjectsKeysApi->delete(
    $projectId,
    $keyId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'DeleteProjectKeyV1Response:';
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

