# Speak V1 Audio

```php
$speakV1AudioApi = $client->getSpeakV1AudioApi();
```

## Class Name

`SpeakV1AudioApi`


# Generate

Convert text into natural-sounding speech using Deepgram's TTS REST API

:information_source: **Note** This endpoint does not require authentication.

```php
function generate(
    string $authorization,
    ?string $callback = null,
    ?string $callbackMethod = V1ListenPostParametersCallbackMethod::POST,
    ?bool $mipOptOut = false,
    $tag = null,
    $bitRate = null,
    ?string $container = null,
    ?string $encoding = null,
    ?string $model = V1SpeakPostParametersModel::AURAASTERIAEN,
    ?string $sampleRate = null,
    ?float $speed = 1,
    ?SpeakV1Request $body = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |
| `callback` | `?string` | Query, Optional | URL to which we'll make the callback request |
| `callbackMethod` | [`?string(V1ListenPostParametersCallbackMethod)`](../../doc/models/v1-listen-post-parameters-callback-method.md) | Query, Optional | HTTP method by which the callback request will be made<br><br>**Default**: `V1ListenPostParametersCallbackMethod::POST` |
| `mipOptOut` | `?bool` | Query, Optional | Opts out requests from the Deepgram Model Improvement Program. Refer to our Docs for pricing impacts before setting this to true. https://dpgr.am/deepgram-mip<br><br>**Default**: `false` |
| `tag` | string\|string[]\|null | Query, Optional | Label your requests for the purpose of identification during usage reporting |
| `bitRate` | string([V1SpeakPostParametersBitRate0](../../doc/models/v1-speak-post-parameters-bit-rate-0.md))\|float\|null | Query, Optional | This is a container for one-of cases. |
| `container` | string([V1SpeakPostParametersContainer0](../../doc/models/v1-speak-post-parameters-container-0.md))\|string([V1SpeakPostParametersContainer1](../../doc/models/v1-speak-post-parameters-container-1.md))\|string([V1SpeakPostParametersContainer2](../../doc/models/v1-speak-post-parameters-container-2.md))\|string([V1SpeakPostParametersContainer3](../../doc/models/v1-speak-post-parameters-container-3.md))\|string([V1SpeakPostParametersContainer4](../../doc/models/v1-speak-post-parameters-container-4.md))\|null | Query, Optional | This is a container for one-of cases. |
| `encoding` | string([V1SpeakPostParametersEncoding0](../../doc/models/v1-speak-post-parameters-encoding-0.md))\|string([V1SpeakPostParametersEncoding1](../../doc/models/v1-speak-post-parameters-encoding-1.md))\|string([V1SpeakPostParametersEncoding2](../../doc/models/v1-speak-post-parameters-encoding-2.md))\|string([V1SpeakPostParametersEncoding3](../../doc/models/v1-speak-post-parameters-encoding-3.md))\|string([V1SpeakPostParametersEncoding4](../../doc/models/v1-speak-post-parameters-encoding-4.md))\|string([V1SpeakPostParametersEncoding5](../../doc/models/v1-speak-post-parameters-encoding-5.md))\|string([V1SpeakPostParametersEncoding6](../../doc/models/v1-speak-post-parameters-encoding-6.md))\|null | Query, Optional | This is a container for one-of cases. |
| `model` | [`?string(V1SpeakPostParametersModel)`](../../doc/models/v1-speak-post-parameters-model.md) | Query, Optional | AI model used to process submitted text<br><br>**Default**: `V1SpeakPostParametersModel::AURAASTERIAEN` |
| `sampleRate` | string([V1SpeakPostParametersSampleRate0](../../doc/models/v1-speak-post-parameters-sample-rate-0.md))\|string([V1SpeakPostParametersSampleRate1](../../doc/models/v1-speak-post-parameters-sample-rate-1.md))\|string([V1SpeakPostParametersSampleRate2](../../doc/models/v1-speak-post-parameters-sample-rate-2.md))\|string([V1SpeakPostParametersSampleRate3](../../doc/models/v1-speak-post-parameters-sample-rate-3.md))\|string([V1SpeakPostParametersSampleRate4](../../doc/models/v1-speak-post-parameters-sample-rate-4.md))\|null | Query, Optional | This is a container for one-of cases. |
| `speed` | `?float` | Query, Optional | Speaking rate multiplier that adjusts the pace of generated speech while preserving natural prosody and voice quality. Not yet supported in all languages.<br><br>**Default**: `1` |
| `body` | [`?SpeakV1Request`](../../doc/models/speak-v1-request.md) | Body, Optional | Transform text to speech |

## Response Type

**200**: Successful text-to-speech transformation

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type `array`.

## Example Usage

```php
$authorization = 'Authorization8';

$callbackMethod = V1ListenPostParametersCallbackMethod::POST;

$mipOptOut = false;

$model = V1SpeakPostParametersModel::AURAASTERIAEN;

$speed = 1;

$speakV1AudioApi = $client->getSpeakV1AudioApi();
$apiResponse = $speakV1AudioApi->generate(
    $authorization,
    null,
    $callbackMethod,
    $mipOptOut,
    null,
    null,
    null,
    null,
    $model,
    null,
    $speed
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

