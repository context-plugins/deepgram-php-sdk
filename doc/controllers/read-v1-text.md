# Read V1 Text

```php
$readV1TextApi = $client->getReadV1TextApi();
```

## Class Name

`ReadV1TextApi`


# Analyze

Analyze text content using Deepgrams text analysis API

:information_source: **Note** This endpoint does not require authentication.

```php
function analyze(
    string $authorization,
    ?string $callback = null,
    ?string $callbackMethod = V1ListenPostParametersCallbackMethod::POST,
    ?bool $sentiment = false,
    $summarize = null,
    $tag = null,
    ?bool $topics = false,
    $customTopic = null,
    ?string $customTopicMode = V1ListenPostParametersCustomTopicMode::EXTENDED,
    ?bool $intents = false,
    $customIntent = null,
    ?string $customIntentMode = V1ListenPostParametersCustomTopicMode::EXTENDED,
    ?string $language = 'en',
    $body = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |
| `callback` | `?string` | Query, Optional | URL to which we'll make the callback request |
| `callbackMethod` | [`?string(V1ListenPostParametersCallbackMethod)`](../../doc/models/v1-listen-post-parameters-callback-method.md) | Query, Optional | HTTP method by which the callback request will be made<br><br>**Default**: `V1ListenPostParametersCallbackMethod::POST` |
| `sentiment` | `?bool` | Query, Optional | Recognizes the sentiment throughout a transcript or text<br><br>**Default**: `false` |
| `summarize` | string([V1ReadPostParametersSummarize0](../../doc/models/v1-read-post-parameters-summarize-0.md))\|bool\|null | Query, Optional | Summarize content. For Listen API, supports string version option. For Read API, accepts boolean only. |
| `tag` | string\|string[]\|null | Query, Optional | Label your requests for the purpose of identification during usage reporting |
| `topics` | `?bool` | Query, Optional | Detect topics throughout a transcript or text<br><br>**Default**: `false` |
| `customTopic` | string\|string[]\|null | Query, Optional | Custom topics you want the model to detect within your input audio or text if present Submit up to `100`. |
| `customTopicMode` | [`?string(V1ListenPostParametersCustomTopicMode)`](../../doc/models/v1-listen-post-parameters-custom-topic-mode.md) | Query, Optional | Sets how the model will interpret strings submitted to the `custom_topic` param. When `strict`, the model will only return topics submitted using the `custom_topic` param. When `extended`, the model will return its own detected topics in addition to those submitted using the `custom_topic` param<br><br>**Default**: `V1ListenPostParametersCustomTopicMode::EXTENDED` |
| `intents` | `?bool` | Query, Optional | Recognizes speaker intent throughout a transcript or text<br><br>**Default**: `false` |
| `customIntent` | string\|string[]\|null | Query, Optional | Custom intents you want the model to detect within your input audio if present |
| `customIntentMode` | [`?string(V1ListenPostParametersCustomTopicMode)`](../../doc/models/v1-listen-post-parameters-custom-topic-mode.md) | Query, Optional | Sets how the model will interpret intents submitted to the `custom_intent` param. When `strict`, the model will only return intents submitted using the `custom_intent` param. When `extended`, the model will return its own detected intents in the `custom_intent` param.<br><br>**Default**: `V1ListenPostParametersCustomTopicMode::EXTENDED` |
| `language` | `?string` | Query, Optional | The [BCP-47 language tag](https://tools.ietf.org/html/bcp47) that hints at the primary spoken language. Depending on the Model and API endpoint you choose only certain languages are available<br><br>**Default**: `'en'` |
| `body` | [ReadV1RequestUrl](../../doc/models/read-v1-request-url.md)\|[ReadV1RequestText](../../doc/models/read-v1-request-text.md)\|null | Body, Optional | Analyze a text file |

## Response Type

**200**: Successful text analysis

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ReadV1Response`](../../doc/models/read-v1-response.md).

## Example Usage

```php
$authorization = 'Authorization8';

$callbackMethod = V1ListenPostParametersCallbackMethod::POST;

$sentiment = false;

$summarize = false;

$topics = false;

$customTopicMode = V1ListenPostParametersCustomTopicMode::EXTENDED;

$intents = false;

$customIntentMode = V1ListenPostParametersCustomTopicMode::EXTENDED;

$language = 'en';

$readV1TextApi = $client->getReadV1TextApi();
$apiResponse = $readV1TextApi->analyze(
    $authorization,
    null,
    $callbackMethod,
    $sentiment,
    $summarize,
    null,
    $topics,
    null,
    $customTopicMode,
    $intents,
    null,
    $customIntentMode,
    $language
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ReadV1Response:';
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

