# Voice Agent Variables

```php
$voiceAgentVariablesApi = $client->getVoiceAgentVariablesApi();
```

## Class Name

`VoiceAgentVariablesApi`

## Methods

* [Create](../../doc/controllers/voice-agent-variables.md#create)
* [List](../../doc/controllers/voice-agent-variables.md#list)
* [Get](../../doc/controllers/voice-agent-variables.md#get)
* [Update](../../doc/controllers/voice-agent-variables.md#update)
* [Delete](../../doc/controllers/voice-agent-variables.md#delete)


# Create

Creates a new template variable. Variables follow the `DG_<VARIABLE_NAME>` naming format and can substitute any JSON value in an agent configuration.

:information_source: **Note** This endpoint does not require authentication.

```php
function create(
    string $projectId,
    string $authorization,
    ?CreateAgentVariableV1Request $body = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |
| `body` | [`?CreateAgentVariableV1Request`](../../doc/models/create-agent-variable-v1-request.md) | Body, Optional | Agent variable details |

## Response Type

**200**: Agent variable created successfully

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`AgentVariableV1`](../../doc/models/agent-variable-v1.md).

## Example Usage

```php
$projectId = 'project_id6';

$authorization = 'Authorization8';

$body = CreateAgentVariableV1RequestBuilder::init(
    'key6',
    ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
)
    ->apiVersion(1)
    ->build();

$voiceAgentVariablesApi = $client->getVoiceAgentVariablesApi();
$apiResponse = $voiceAgentVariablesApi->create(
    $projectId,
    $authorization,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'AgentVariableV1:';
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


# List

Returns all template variables for the specified project

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

**200**: A list of agent variables

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ListAgentVariablesV1Response`](../../doc/models/list-agent-variables-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$authorization = 'Authorization8';

$voiceAgentVariablesApi = $client->getVoiceAgentVariablesApi();
$apiResponse = $voiceAgentVariablesApi->mList(
    $projectId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ListAgentVariablesV1Response:';
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

Returns the specified template variable

:information_source: **Note** This endpoint does not require authentication.

```php
function get(string $projectId, string $variableId, string $authorization): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `variableId` | `string` | Template, Required | The unique identifier of the agent variable |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |

## Response Type

**200**: An agent variable

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`AgentVariableV1`](../../doc/models/agent-variable-v1.md).

## Example Usage

```php
$projectId = 'project_id6';

$variableId = 'variable_id8';

$authorization = 'Authorization8';

$voiceAgentVariablesApi = $client->getVoiceAgentVariablesApi();
$apiResponse = $voiceAgentVariablesApi->get(
    $projectId,
    $variableId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'AgentVariableV1:';
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

Updates the value of an existing template variable

:information_source: **Note** This endpoint does not require authentication.

```php
function update(
    string $projectId,
    string $variableId,
    string $authorization,
    ?UpdateAgentVariableV1Request $body = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `variableId` | `string` | Template, Required | The unique identifier of the agent variable |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |
| `body` | [`?UpdateAgentVariableV1Request`](../../doc/models/update-agent-variable-v1-request.md) | Body, Optional | Updated value for the agent variable |

## Response Type

**200**: Agent variable updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`AgentVariableV1`](../../doc/models/agent-variable-v1.md).

## Example Usage

```php
$projectId = 'project_id6';

$variableId = 'variable_id8';

$authorization = 'Authorization8';

$voiceAgentVariablesApi = $client->getVoiceAgentVariablesApi();
$apiResponse = $voiceAgentVariablesApi->update(
    $projectId,
    $variableId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'AgentVariableV1:';
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

Deletes the specified template variable

:information_source: **Note** This endpoint does not require authentication.

```php
function delete(string $projectId, string $variableId, string $authorization): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `variableId` | `string` | Template, Required | The unique identifier of the agent variable |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |

## Response Type

**200**: Agent variable deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type `array`.

## Example Usage

```php
$projectId = 'project_id6';

$variableId = 'variable_id8';

$authorization = 'Authorization8';

$voiceAgentVariablesApi = $client->getVoiceAgentVariablesApi();
$apiResponse = $voiceAgentVariablesApi->delete(
    $projectId,
    $variableId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'array:';
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

