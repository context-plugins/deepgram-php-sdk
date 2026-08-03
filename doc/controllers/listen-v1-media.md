# Listen V1 Media

```php
$listenV1MediaApi = $client->getListenV1MediaApi();
```

## Class Name

`ListenV1MediaApi`


# Transcribe

Transcribe audio and video using Deepgram's speech-to-text REST API

:information_source: **Note** This endpoint does not require authentication.

```php
function transcribe(
    string $authorization,
    ?string $callback = null,
    ?string $callbackMethod = V1ListenPostParametersCallbackMethod::POST,
    $extra = null,
    ?bool $sentiment = false,
    $summarize = null,
    $tag = null,
    ?bool $topics = false,
    $customTopic = null,
    ?string $customTopicMode = V1ListenPostParametersCustomTopicMode::EXTENDED,
    ?bool $intents = false,
    $customIntent = null,
    ?string $customIntentMode = V1ListenPostParametersCustomTopicMode::EXTENDED,
    ?bool $detectEntities = false,
    $detectLanguage = null,
    ?bool $diarize = false,
    ?string $diarizeModel = null,
    ?bool $dictation = false,
    ?string $encoding = null,
    ?bool $fillerWords = false,
    ?array $keyterm = null,
    $keywords = null,
    ?string $language = 'en',
    ?bool $measurements = false,
    ?string $model = null,
    ?bool $multichannel = false,
    ?bool $numerals = false,
    ?bool $paragraphs = false,
    ?bool $profanityFilter = false,
    ?bool $punctuate = false,
    $redact = null,
    $replace = null,
    $search = null,
    ?bool $smartFormat = false,
    ?bool $utterances = false,
    ?float $uttSplit = 0.8,
    ?string $version = null,
    ?bool $mipOptOut = false,
    ?ListenV1RequestUrl $body = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |
| `callback` | `?string` | Query, Optional | URL to which we'll make the callback request |
| `callbackMethod` | [`?string(V1ListenPostParametersCallbackMethod)`](../../doc/models/v1-listen-post-parameters-callback-method.md) | Query, Optional | HTTP method by which the callback request will be made<br><br>**Default**: `V1ListenPostParametersCallbackMethod::POST` |
| `extra` | string\|string[]\|null | Query, Optional | Arbitrary key-value pairs that are attached to the API response for usage in downstream processing |
| `sentiment` | `?bool` | Query, Optional | Recognizes the sentiment throughout a transcript or text<br><br>**Default**: `false` |
| `summarize` | string([V1ListenPostParametersSummarize0](../../doc/models/v1-listen-post-parameters-summarize-0.md))\|bool\|null | Query, Optional | Summarize content. For Listen API, supports string version option. For Read API, accepts boolean only. |
| `tag` | string\|string[]\|null | Query, Optional | Label your requests for the purpose of identification during usage reporting |
| `topics` | `?bool` | Query, Optional | Detect topics throughout a transcript or text<br><br>**Default**: `false` |
| `customTopic` | string\|string[]\|null | Query, Optional | Custom topics you want the model to detect within your input audio or text if present Submit up to `100`. |
| `customTopicMode` | [`?string(V1ListenPostParametersCustomTopicMode)`](../../doc/models/v1-listen-post-parameters-custom-topic-mode.md) | Query, Optional | Sets how the model will interpret strings submitted to the `custom_topic` param. When `strict`, the model will only return topics submitted using the `custom_topic` param. When `extended`, the model will return its own detected topics in addition to those submitted using the `custom_topic` param<br><br>**Default**: `V1ListenPostParametersCustomTopicMode::EXTENDED` |
| `intents` | `?bool` | Query, Optional | Recognizes speaker intent throughout a transcript or text<br><br>**Default**: `false` |
| `customIntent` | string\|string[]\|null | Query, Optional | Custom intents you want the model to detect within your input audio if present |
| `customIntentMode` | [`?string(V1ListenPostParametersCustomTopicMode)`](../../doc/models/v1-listen-post-parameters-custom-topic-mode.md) | Query, Optional | Sets how the model will interpret intents submitted to the `custom_intent` param. When `strict`, the model will only return intents submitted using the `custom_intent` param. When `extended`, the model will return its own detected intents in the `custom_intent` param.<br><br>**Default**: `V1ListenPostParametersCustomTopicMode::EXTENDED` |
| `detectEntities` | `?bool` | Query, Optional | Identifies and extracts key entities from content in submitted audio<br><br>**Default**: `false` |
| `detectLanguage` | bool\|string[]\|null | Query, Optional | Identifies the dominant language spoken in submitted audio |
| `diarize` | `?bool` | Query, Optional | Deprecated: use `diarize_model` instead. Recognize speaker changes. Each word in the transcript will be assigned a speaker number starting at 0.<br><br>**Default**: `false` |
| `diarizeModel` | [`?string(V1ListenPostParametersDiarizeModel)`](../../doc/models/v1-listen-post-parameters-diarize-model.md) | Query, Optional | Select and enable a specific diarization model version. Specifying this parameter enables diarization and selects the model — you do not need to also set the deprecated `diarize=true` parameter. For batch, supported values are `latest` (currently v2), `v1`, and `v2`. For streaming, supported values are `latest` (currently v1) and `v1`; `v2` returns a validation error on streaming requests. |
| `dictation` | `?bool` | Query, Optional | Dictation mode for controlling formatting with dictated speech<br><br>**Default**: `false` |
| `encoding` | [`?string(V1ListenPostParametersEncoding)`](../../doc/models/v1-listen-post-parameters-encoding.md) | Query, Optional | Specify the expected encoding of your submitted audio |
| `fillerWords` | `?bool` | Query, Optional | Filler Words can help transcribe interruptions in your audio, like "uh" and "um"<br><br>**Default**: `false` |
| `keyterm` | `?(string[])` | Query, Optional | Key term prompting improves recognition of specialized terminology and brands. Only compatible with Nova-3.<br><br>`keyterm` accepts plain terms only. Unlike the legacy `keywords` feature, it does not support weights or intensifiers. Appending one (for example, `keyterm=term:0.15`) is not rejected—the weight is silently ignored and the entire value is treated as a literal keyterm.<br><br>To boost multiple separate keyterms, repeat the `keyterm` parameter (for example, `keyterm=term1&keyterm=term2`). To boost one multi-word phrase as a single keyterm, join the words with `%20` or `+` (for example, `keyterm=customer%20service`). Do not separate keyterms with commas, semicolons, or line breaks. |
| `keywords` | string\|string[]\|null | Query, Optional | Keywords can boost or suppress specialized terminology and brands |
| `language` | `?string` | Query, Optional | The [BCP-47 language tag](https://tools.ietf.org/html/bcp47) that hints at the primary spoken language. Depending on the Model and API endpoint you choose only certain languages are available<br><br>**Default**: `'en'` |
| `measurements` | `?bool` | Query, Optional | Spoken measurements will be converted to their corresponding abbreviations<br><br>**Default**: `false` |
| `model` | string([V1ListenPostParametersModel0](../../doc/models/v1-listen-post-parameters-model-0.md))\|string\|null | Query, Optional | This is a container for one-of cases. |
| `multichannel` | `?bool` | Query, Optional | Transcribe each audio channel independently<br><br>**Default**: `false` |
| `numerals` | `?bool` | Query, Optional | Numerals converts numbers from written format to numerical format<br><br>**Default**: `false` |
| `paragraphs` | `?bool` | Query, Optional | Splits audio into paragraphs to improve transcript readability<br><br>**Default**: `false` |
| `profanityFilter` | `?bool` | Query, Optional | Profanity Filter looks for recognized profanity and converts it to the nearest recognized non-profane word or removes it from the transcript completely<br><br>**Default**: `false` |
| `punctuate` | `?bool` | Query, Optional | Add punctuation and capitalization to the transcript<br><br>**Default**: `false` |
| `redact` | string\|string([V1ListenPostParametersRedactSchemaOneOf1Items](../../doc/models/v1-listen-post-parameters-redact-schema-one-of-1-items.md))[]\|null | Query, Optional | This is a container for one-of cases. |
| `replace` | string\|string[]\|null | Query, Optional | Search for terms or phrases in submitted audio and replaces them |
| `search` | string\|string[]\|null | Query, Optional | Search for terms or phrases in submitted audio |
| `smartFormat` | `?bool` | Query, Optional | Apply formatting to transcript output. When set to true, additional formatting will be applied to transcripts to improve readability<br><br>**Default**: `false` |
| `utterances` | `?bool` | Query, Optional | Segments speech into meaningful semantic units<br><br>**Default**: `false` |
| `uttSplit` | `?float` | Query, Optional | Seconds to wait before detecting a pause between words in submitted audio<br><br>**Default**: `0.8` |
| `version` | string([V1ListenPostParametersVersion0](../../doc/models/v1-listen-post-parameters-version-0.md))\|string\|null | Query, Optional | This is a container for one-of cases. |
| `mipOptOut` | `?bool` | Query, Optional | Opts out requests from the Deepgram Model Improvement Program. Refer to our Docs for pricing impacts before setting this to true. https://dpgr.am/deepgram-mip<br><br>**Default**: `false` |
| `body` | [`?ListenV1RequestUrl`](../../doc/models/listen-v1-request-url.md) | Body, Optional | Transcribe an audio or video file |

## Response Type

**200**: Returns either transcription results, or a request_id when using a callback.

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type `ListenV1Response|ListenV1AcceptedResponse`.

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

$detectEntities = false;

$detectLanguage = false;

$diarize = false;

$dictation = false;

$fillerWords = false;

$language = 'en';

$measurements = false;

$multichannel = false;

$numerals = false;

$paragraphs = false;

$profanityFilter = false;

$punctuate = false;

$smartFormat = false;

$utterances = false;

$uttSplit = 0.8;

$mipOptOut = false;

$listenV1MediaApi = $client->getListenV1MediaApi();
$apiResponse = $listenV1MediaApi->transcribe(
    $authorization,
    null,
    $callbackMethod,
    null,
    $sentiment,
    $summarize,
    null,
    $topics,
    null,
    $customTopicMode,
    $intents,
    null,
    $customIntentMode,
    $detectEntities,
    $detectLanguage,
    $diarize,
    null,
    $dictation,
    null,
    $fillerWords,
    null,
    null,
    $language,
    $measurements,
    null,
    $multichannel,
    $numerals,
    $paragraphs,
    $profanityFilter,
    $punctuate,
    null,
    null,
    null,
    $smartFormat,
    $utterances,
    $uttSplit,
    null,
    $mipOptOut
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ListenV1Response|ListenV1AcceptedResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid Request | [`ListenV1ResponseErrorException`](../../doc/models/listen-v1-response-error-exception.md) |

