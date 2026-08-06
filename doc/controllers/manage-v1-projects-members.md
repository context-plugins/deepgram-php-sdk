# Manage V1 Projects Members

```php
$manageV1ProjectsMembersApi = $client->getManageV1ProjectsMembersApi();
```

## Class Name

`ManageV1ProjectsMembersApi`

## Methods

* [List](../../doc/controllers/manage-v1-projects-members.md#list)
* [Delete](../../doc/controllers/manage-v1-projects-members.md#delete)


# List

Retrieves a list of members for a given project

```php
function mList(string $projectId): ApiResponse
```

## Authentication

This endpoint requires [ApiKeyAuth](../../doc/auth/custom-header-signature.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |

## Response Type

**200**: A list of members for a given project

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ListProjectMembersV1Response`](../../doc/models/list-project-members-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$manageV1ProjectsMembersApi = $client->getManageV1ProjectsMembersApi();
$apiResponse = $manageV1ProjectsMembersApi->mList($projectId);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ListProjectMembersV1Response:';
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

Removes a member from the project using their unique member ID

```php
function delete(string $projectId, string $memberId): ApiResponse
```

## Authentication

This endpoint requires [ApiKeyAuth](../../doc/auth/custom-header-signature.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `memberId` | `string` | Template, Required | The unique identifier of the Member |

## Response Type

**200**: Delete the specific member from the project

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`DeleteProjectMemberV1Response`](../../doc/models/delete-project-member-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$memberId = 'member_id0';

$manageV1ProjectsMembersApi = $client->getManageV1ProjectsMembersApi();
$apiResponse = $manageV1ProjectsMembersApi->delete(
    $projectId,
    $memberId
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'DeleteProjectMemberV1Response:';
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

