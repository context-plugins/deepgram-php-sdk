# Manage V1 Projects Usage

```php
$manageV1ProjectsUsageApi = $client->getManageV1ProjectsUsageApi();
```

## Class Name

`ManageV1ProjectsUsageApi`


# Get

Retrieves the usage for a specific project. Use Get Project Usage Breakdown for a more comprehensive usage summary.

:information_source: **Note** This endpoint does not require authentication.

```php
function get(
    string $projectId,
    string $authorization,
    ?\DateTime $start = null,
    ?\DateTime $end = null,
    ?string $accessor = null,
    ?bool $alternatives = null,
    ?bool $callbackMethod = null,
    ?bool $callback = null,
    ?bool $channels = null,
    ?bool $customIntentMode = null,
    ?bool $customIntent = null,
    ?bool $customTopicMode = null,
    ?bool $customTopic = null,
    ?string $deployment = null,
    ?bool $detectEntities = null,
    ?bool $detectLanguage = null,
    ?bool $diarize = null,
    ?bool $dictation = null,
    ?bool $encoding = null,
    ?string $endpoint = null,
    ?bool $extra = null,
    ?bool $fillerWords = null,
    ?bool $intents = null,
    ?bool $keyterm = null,
    ?bool $keywords = null,
    ?bool $language = null,
    ?bool $measurements = null,
    ?string $method = null,
    ?string $model = null,
    ?bool $multichannel = null,
    ?bool $numerals = null,
    ?bool $paragraphs = null,
    ?bool $profanityFilter = null,
    ?bool $punctuate = null,
    ?bool $redact = null,
    ?bool $replace = null,
    ?bool $sampleRate = null,
    ?bool $search = null,
    ?bool $sentiment = null,
    ?bool $smartFormat = null,
    ?bool $summarize = null,
    ?string $tag = null,
    ?bool $topics = null,
    ?bool $uttSplit = null,
    ?bool $utterances = null,
    ?bool $version = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |
| `start` | `?DateTime` | Query, Optional | Start date of the requested date range. Format accepted is YYYY-MM-DD |
| `end` | `?DateTime` | Query, Optional | End date of the requested date range. Format accepted is YYYY-MM-DD |
| `accessor` | `?string` | Query, Optional | Filter for requests where a specific accessor was used |
| `alternatives` | `?bool` | Query, Optional | Filter for requests where alternatives were used |
| `callbackMethod` | `?bool` | Query, Optional | Filter for requests where callback method was used |
| `callback` | `?bool` | Query, Optional | Filter for requests where callback was used |
| `channels` | `?bool` | Query, Optional | Filter for requests where channels were used |
| `customIntentMode` | `?bool` | Query, Optional | Filter for requests where custom intent mode was used |
| `customIntent` | `?bool` | Query, Optional | Filter for requests where custom intent was used |
| `customTopicMode` | `?bool` | Query, Optional | Filter for requests where custom topic mode was used |
| `customTopic` | `?bool` | Query, Optional | Filter for requests where custom topic was used |
| `deployment` | [`?string(V1ProjectsProjectIdUsageGetParametersDeployment)`](../../doc/models/v1-projects-project-id-usage-get-parameters-deployment.md) | Query, Optional | Filter for requests where a specific deployment was used |
| `detectEntities` | `?bool` | Query, Optional | Filter for requests where detect entities was used |
| `detectLanguage` | `?bool` | Query, Optional | Filter for requests where detect language was used |
| `diarize` | `?bool` | Query, Optional | Filter for requests where diarize was used |
| `dictation` | `?bool` | Query, Optional | Filter for requests where dictation was used |
| `encoding` | `?bool` | Query, Optional | Filter for requests where encoding was used |
| `endpoint` | [`?string(V1ProjectsProjectIdUsageGetParametersEndpoint)`](../../doc/models/v1-projects-project-id-usage-get-parameters-endpoint.md) | Query, Optional | Filter for requests where a specific endpoint was used |
| `extra` | `?bool` | Query, Optional | Filter for requests where extra was used |
| `fillerWords` | `?bool` | Query, Optional | Filter for requests where filler words was used |
| `intents` | `?bool` | Query, Optional | Filter for requests where intents was used |
| `keyterm` | `?bool` | Query, Optional | Filter for requests where keyterm was used |
| `keywords` | `?bool` | Query, Optional | Filter for requests where keywords was used |
| `language` | `?bool` | Query, Optional | Filter for requests where language was used |
| `measurements` | `?bool` | Query, Optional | Filter for requests where measurements were used |
| `method` | [`?string(V1ProjectsProjectIdUsageGetParametersMethod)`](../../doc/models/v1-projects-project-id-usage-get-parameters-method.md) | Query, Optional | Filter for requests where a specific method was used |
| `model` | `?string` | Query, Optional | Filter for requests where a specific model uuid was used |
| `multichannel` | `?bool` | Query, Optional | Filter for requests where multichannel was used |
| `numerals` | `?bool` | Query, Optional | Filter for requests where numerals were used |
| `paragraphs` | `?bool` | Query, Optional | Filter for requests where paragraphs were used |
| `profanityFilter` | `?bool` | Query, Optional | Filter for requests where profanity filter was used |
| `punctuate` | `?bool` | Query, Optional | Filter for requests where punctuate was used |
| `redact` | `?bool` | Query, Optional | Filter for requests where redact was used |
| `replace` | `?bool` | Query, Optional | Filter for requests where replace was used |
| `sampleRate` | `?bool` | Query, Optional | Filter for requests where sample rate was used |
| `search` | `?bool` | Query, Optional | Filter for requests where search was used |
| `sentiment` | `?bool` | Query, Optional | Filter for requests where sentiment was used |
| `smartFormat` | `?bool` | Query, Optional | Filter for requests where smart format was used |
| `summarize` | `?bool` | Query, Optional | Filter for requests where summarize was used |
| `tag` | `?string` | Query, Optional | Filter for requests where a specific tag was used |
| `topics` | `?bool` | Query, Optional | Filter for requests where topics was used |
| `uttSplit` | `?bool` | Query, Optional | Filter for requests where utt split was used |
| `utterances` | `?bool` | Query, Optional | Filter for requests where utterances was used |
| `version` | `?bool` | Query, Optional | Filter for requests where version was used |

## Response Type

**200**: A specific request for a specific project

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`UsageV1Response`](../../doc/models/usage-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$authorization = 'Authorization8';

$manageV1ProjectsUsageApi = $client->getManageV1ProjectsUsageApi();
$apiResponse = $manageV1ProjectsUsageApi->get(
    $projectId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'UsageV1Response:';
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

