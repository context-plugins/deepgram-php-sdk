# Manage V1 Projects Models

```php
$manageV1ProjectsModelsApi = $client->getManageV1ProjectsModelsApi();
```

## Class Name

`ManageV1ProjectsModelsApi`

## Methods

* [List](../../doc/controllers/manage-v1-projects-models.md#list)
* [Get](../../doc/controllers/manage-v1-projects-models.md#get)


# List

Returns metadata on all the latest models that a specific project has access to, including non-public models

:information_source: **Note** This endpoint does not require authentication.

```php
function mList(string $projectId, string $authorization, ?bool $includeOutdated = null): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |
| `includeOutdated` | `?bool` | Query, Optional | returns non-latest versions of models |

## Response Type

**200**: A list of models

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ListModelsV1Response`](../../doc/models/list-models-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$authorization = 'Authorization8';

$manageV1ProjectsModelsApi = $client->getManageV1ProjectsModelsApi();
$apiResponse = $manageV1ProjectsModelsApi->mList(
    $projectId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ListModelsV1Response:';
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

Returns metadata for a specific model

:information_source: **Note** This endpoint does not require authentication.

```php
function get(string $projectId, string $modelId, string $authorization): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `modelId` | `string` | Template, Required | The specific UUID of the model |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |

## Response Type

**200**: A model object that can be either STT or TTS

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type `GetModelV1Response0|GetModelV1Response1`.

## Example Usage

```php
$projectId = 'project_id6';

$modelId = 'model_id0';

$authorization = 'Authorization8';

$manageV1ProjectsModelsApi = $client->getManageV1ProjectsModelsApi();
$apiResponse = $manageV1ProjectsModelsApi->get(
    $projectId,
    $modelId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'GetModelV1Response0|GetModelV1Response1:';
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

