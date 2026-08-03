# Self Hosted V1 Distribution Credentials

```php
$selfHostedV1DistributionCredentialsApi = $client->getSelfHostedV1DistributionCredentialsApi();
```

## Class Name

`SelfHostedV1DistributionCredentialsApi`

## Methods

* [List](../../doc/controllers/self-hosted-v1-distribution-credentials.md#list)
* [Create](../../doc/controllers/self-hosted-v1-distribution-credentials.md#create)
* [Get](../../doc/controllers/self-hosted-v1-distribution-credentials.md#get)
* [Delete](../../doc/controllers/self-hosted-v1-distribution-credentials.md#delete)


# List

Lists sets of distribution credentials for the specified project

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

**200**: A list of distribution credentials for a specific project

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ListProjectDistributionCredentialsV1Response`](../../doc/models/list-project-distribution-credentials-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$authorization = 'Authorization8';

$selfHostedV1DistributionCredentialsApi = $client->getSelfHostedV1DistributionCredentialsApi();
$apiResponse = $selfHostedV1DistributionCredentialsApi->mList(
    $projectId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ListProjectDistributionCredentialsV1Response:';
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

Creates a set of distribution credentials for the specified project

:information_source: **Note** This endpoint does not require authentication.

```php
function create(
    string $projectId,
    string $authorization,
    ?array $scopes = null,
    ?string $provider = V1ProjectsProjectIdSelfHostedDistributionCredentialsPostParametersProvider::QUAY,
    ?CreateProjectDistributionCredentialsV1Request $body = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |
| `scopes` | [`?(string(V1ProjectsProjectIdSelfHostedDistributionCredentialsPostParametersScopesSchemaItems)[])`](../../doc/models/v1-projects-project-id-self-hosted-distribution-credentials-post-parameters-scopes-schema-items.md) | Query, Optional | List of permission scopes for the credentials |
| `provider` | [`?string(V1ProjectsProjectIdSelfHostedDistributionCredentialsPostParametersProvider)`](../../doc/models/v1-projects-project-id-self-hosted-distribution-credentials-post-parameters-provider.md) | Query, Optional | The provider of the distribution service<br><br>**Default**: `V1ProjectsProjectIdSelfHostedDistributionCredentialsPostParametersProvider::QUAY` |
| `body` | [`?CreateProjectDistributionCredentialsV1Request`](../../doc/models/create-project-distribution-credentials-v1-request.md) | Body, Optional | The set of distribution credentials to create |

## Response Type

**200**: Single distribution credential

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`CreateProjectDistributionCredentialsV1Response`](../../doc/models/create-project-distribution-credentials-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$authorization = 'Authorization8';

$provider = V1ProjectsProjectIdSelfHostedDistributionCredentialsPostParametersProvider::QUAY;

$selfHostedV1DistributionCredentialsApi = $client->getSelfHostedV1DistributionCredentialsApi();
$apiResponse = $selfHostedV1DistributionCredentialsApi->create(
    $projectId,
    $authorization,
    null,
    $provider
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'CreateProjectDistributionCredentialsV1Response:';
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

Returns a set of distribution credentials for the specified project

:information_source: **Note** This endpoint does not require authentication.

```php
function get(string $projectId, string $distributionCredentialsId, string $authorization): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `distributionCredentialsId` | `string` | Template, Required | The UUID of the distribution credentials |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |

## Response Type

**200**: Single distribution credential

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`GetProjectDistributionCredentialsV1Response`](../../doc/models/get-project-distribution-credentials-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$distributionCredentialsId = 'distribution_credentials_id0';

$authorization = 'Authorization8';

$selfHostedV1DistributionCredentialsApi = $client->getSelfHostedV1DistributionCredentialsApi();
$apiResponse = $selfHostedV1DistributionCredentialsApi->get(
    $projectId,
    $distributionCredentialsId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'GetProjectDistributionCredentialsV1Response:';
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

Deletes a set of distribution credentials for the specified project

:information_source: **Note** This endpoint does not require authentication.

```php
function delete(string $projectId, string $distributionCredentialsId, string $authorization): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `distributionCredentialsId` | `string` | Template, Required | The UUID of the distribution credentials |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |

## Response Type

**200**: Single distribution credential

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`GetProjectDistributionCredentialsV1Response`](../../doc/models/get-project-distribution-credentials-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$distributionCredentialsId = 'distribution_credentials_id0';

$authorization = 'Authorization8';

$selfHostedV1DistributionCredentialsApi = $client->getSelfHostedV1DistributionCredentialsApi();
$apiResponse = $selfHostedV1DistributionCredentialsApi->delete(
    $projectId,
    $distributionCredentialsId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'GetProjectDistributionCredentialsV1Response:';
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

