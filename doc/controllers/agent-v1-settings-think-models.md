# Agent V1 Settings Think Models

```php
$agentV1SettingsThinkModelsApi = $client->getAgentV1SettingsThinkModelsApi();
```

## Class Name

`AgentV1SettingsThinkModelsApi`


# List

Retrieves the available think models that can be used for AI agent processing

:information_source: **Note** This endpoint does not require authentication.

```php
function mList(): ApiResponse
```

## Response Type

**200**: List of available think models

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`AgentThinkModelsV1Response`](../../doc/models/agent-think-models-v1-response.md).

## Example Usage

```php
$agentV1SettingsThinkModelsApi = $client->getAgentV1SettingsThinkModelsApi();
$apiResponse = $agentV1SettingsThinkModelsApi->mList();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'AgentThinkModelsV1Response:';
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

