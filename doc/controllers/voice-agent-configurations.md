# Voice Agent Configurations

```php
$voiceAgentConfigurationsApi = $client->getVoiceAgentConfigurationsApi();
```

## Class Name

`VoiceAgentConfigurationsApi`

## Methods

* [Create](../../doc/controllers/voice-agent-configurations.md#create)
* [List](../../doc/controllers/voice-agent-configurations.md#list)
* [Get](../../doc/controllers/voice-agent-configurations.md#get)
* [Update](../../doc/controllers/voice-agent-configurations.md#update)
* [Delete](../../doc/controllers/voice-agent-configurations.md#delete)


# Create

Creates a new reusable agent configuration. The `config` field must be a valid JSON string representing the `agent` block of a Settings message. The returned `agent_id` can be passed in place of the full `agent` object in future Settings messages.

:information_source: **Note** This endpoint does not require authentication.

```php
function create(
    string $projectId,
    string $authorization,
    ?CreateAgentConfigurationV1Request $body = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |
| `body` | [`?CreateAgentConfigurationV1Request`](../../doc/models/create-agent-configuration-v1-request.md) | Body, Optional | Agent configuration details |

## Response Type

**200**: Agent configuration created successfully

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`CreateAgentConfigurationV1Response`](../../doc/models/create-agent-configuration-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$authorization = 'Authorization8';

$body = CreateAgentConfigurationV1RequestBuilder::init(
    'config2'
)
    ->apiVersion(1)
    ->build();

$voiceAgentConfigurationsApi = $client->getVoiceAgentConfigurationsApi();
$apiResponse = $voiceAgentConfigurationsApi->create(
    $projectId,
    $authorization,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'CreateAgentConfigurationV1Response:';
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

Returns all agent configurations for the specified project. Configurations are returned in their uninterpolated form—template variable placeholders appear as-is rather than with their substituted values.

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

**200**: A list of agent configurations

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ListAgentConfigurationsV1Response`](../../doc/models/list-agent-configurations-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$authorization = 'Authorization8';

$voiceAgentConfigurationsApi = $client->getVoiceAgentConfigurationsApi();
$apiResponse = $voiceAgentConfigurationsApi->mList(
    $projectId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ListAgentConfigurationsV1Response:';
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

Returns the specified agent configuration in its uninterpolated form

:information_source: **Note** This endpoint does not require authentication.

```php
function get(string $projectId, string $agentId, string $authorization): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `agentId` | `string` | Template, Required | The unique identifier of the agent configuration |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |

## Response Type

**200**: An agent configuration

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`AgentConfigurationV1`](../../doc/models/agent-configuration-v1.md).

## Example Usage

```php
$projectId = 'project_id6';

$agentId = 'agent_id8';

$authorization = 'Authorization8';

$voiceAgentConfigurationsApi = $client->getVoiceAgentConfigurationsApi();
$apiResponse = $voiceAgentConfigurationsApi->get(
    $projectId,
    $agentId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'AgentConfigurationV1:';
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

Updates the metadata associated with an agent configuration. The config itself is immutable—to change the configuration, delete the existing agent and create a new one.

:information_source: **Note** This endpoint does not require authentication.

```php
function update(
    string $projectId,
    string $agentId,
    string $authorization,
    ?UpdateAgentMetadataV1Request $body = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `agentId` | `string` | Template, Required | The unique identifier of the agent configuration |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |
| `body` | [`?UpdateAgentMetadataV1Request`](../../doc/models/update-agent-metadata-v1-request.md) | Body, Optional | Updated metadata for the agent configuration |

## Response Type

**200**: Agent configuration updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`AgentConfigurationV1`](../../doc/models/agent-configuration-v1.md).

## Example Usage

```php
$projectId = 'project_id6';

$agentId = 'agent_id8';

$authorization = 'Authorization8';

$voiceAgentConfigurationsApi = $client->getVoiceAgentConfigurationsApi();
$apiResponse = $voiceAgentConfigurationsApi->update(
    $projectId,
    $agentId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'AgentConfigurationV1:';
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

Deletes the specified agent configuration. Deleting an agent configuration can cause a production outage if your service references this agent UUID. Migrate all active sessions to a new configuration before deleting.

:information_source: **Note** This endpoint does not require authentication.

```php
function delete(string $projectId, string $agentId, string $authorization): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `agentId` | `string` | Template, Required | The unique identifier of the agent configuration |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |

## Response Type

**200**: Agent configuration deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type `array`.

## Example Usage

```php
$projectId = 'project_id6';

$agentId = 'agent_id8';

$authorization = 'Authorization8';

$voiceAgentConfigurationsApi = $client->getVoiceAgentConfigurationsApi();
$apiResponse = $voiceAgentConfigurationsApi->delete(
    $projectId,
    $agentId,
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

