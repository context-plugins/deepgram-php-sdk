# Manage V1 Projects Members Scopes

```php
$manageV1ProjectsMembersScopesApi = $client->getManageV1ProjectsMembersScopesApi();
```

## Class Name

`ManageV1ProjectsMembersScopesApi`

## Methods

* [List](../../doc/controllers/manage-v1-projects-members-scopes.md#list)
* [Update](../../doc/controllers/manage-v1-projects-members-scopes.md#update)


# List

Retrieves a list of scopes for a specific member

```php
function mList(string $projectId, string $memberId): ApiResponse
```

## Authentication

This endpoint requires [ApiKeyAuth](../../doc/auth/custom-header-signature.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `memberId` | `string` | Template, Required | The unique identifier of the Member |

## Response Type

**200**: A list of scopes for a specific member

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ListProjectMemberScopesV1Response`](../../doc/models/list-project-member-scopes-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$memberId = 'member_id0';

$manageV1ProjectsMembersScopesApi = $client->getManageV1ProjectsMembersScopesApi();
$apiResponse = $manageV1ProjectsMembersScopesApi->mList(
    $projectId,
    $memberId
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ListProjectMemberScopesV1Response:';
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

Updates the scopes for a specific member

```php
function update(
    string $projectId,
    string $memberId,
    ?UpdateProjectMemberScopesV1Request $body = null
): ApiResponse
```

## Authentication

This endpoint requires [ApiKeyAuth](../../doc/auth/custom-header-signature.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `memberId` | `string` | Template, Required | The unique identifier of the Member |
| `body` | [`?UpdateProjectMemberScopesV1Request`](../../doc/models/update-project-member-scopes-v1-request.md) | Body, Optional | A scope to update |

## Response Type

**200**: Updated the scopes for a specific member

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`UpdateProjectMemberScopesV1Response`](../../doc/models/update-project-member-scopes-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$memberId = 'member_id0';

$manageV1ProjectsMembersScopesApi = $client->getManageV1ProjectsMembersScopesApi();
$apiResponse = $manageV1ProjectsMembersScopesApi->update(
    $projectId,
    $memberId
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'UpdateProjectMemberScopesV1Response:';
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

