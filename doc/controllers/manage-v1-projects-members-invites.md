# Manage V1 Projects Members Invites

```php
$manageV1ProjectsMembersInvitesApi = $client->getManageV1ProjectsMembersInvitesApi();
```

## Class Name

`ManageV1ProjectsMembersInvitesApi`

## Methods

* [List](../../doc/controllers/manage-v1-projects-members-invites.md#list)
* [Create](../../doc/controllers/manage-v1-projects-members-invites.md#create)
* [Delete](../../doc/controllers/manage-v1-projects-members-invites.md#delete)


# List

Generates a list of invites for a specific project

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

**200**: A list of invites for a specific project

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ListProjectInvitesV1Response`](../../doc/models/list-project-invites-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$authorization = 'Authorization8';

$manageV1ProjectsMembersInvitesApi = $client->getManageV1ProjectsMembersInvitesApi();
$apiResponse = $manageV1ProjectsMembersInvitesApi->mList(
    $projectId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ListProjectInvitesV1Response:';
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

Generates an invite for a specific project

:information_source: **Note** This endpoint does not require authentication.

```php
function create(
    string $projectId,
    string $authorization,
    ?CreateProjectInviteV1Request $body = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |
| `body` | [`?CreateProjectInviteV1Request`](../../doc/models/create-project-invite-v1-request.md) | Body, Optional | email to invite to the project |

## Response Type

**200**: The invite was successfully generated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`CreateProjectInviteV1Response`](../../doc/models/create-project-invite-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$authorization = 'Authorization8';

$manageV1ProjectsMembersInvitesApi = $client->getManageV1ProjectsMembersInvitesApi();
$apiResponse = $manageV1ProjectsMembersInvitesApi->create(
    $projectId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'CreateProjectInviteV1Response:';
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

Deletes an invite for a specific project

:information_source: **Note** This endpoint does not require authentication.

```php
function delete(string $projectId, string $email, string $authorization): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `email` | `string` | Template, Required | The email address of the member |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |

## Response Type

**200**: The invite was successfully deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`DeleteProjectInviteV1Response`](../../doc/models/delete-project-invite-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$email = 'email6';

$authorization = 'Authorization8';

$manageV1ProjectsMembersInvitesApi = $client->getManageV1ProjectsMembersInvitesApi();
$apiResponse = $manageV1ProjectsMembersInvitesApi->delete(
    $projectId,
    $email,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'DeleteProjectInviteV1Response:';
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

