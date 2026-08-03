
# Speak V2 Request

Request body for Flux TTS batch (REST) text-to-speech conversion. The full block of text is synthesized in a single request and returned as one audio response.

*This model accepts additional fields of type array.*

## Structure

`SpeakV2Request`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `text` | `string` | Required | The text content to be converted to speech. The server normalizes and preprocesses the text (e.g. stripping inline controls) before synthesis. | getText(): string | setText(string text): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\SpeakV2RequestBuilder;
use RestApiLib\ApiHelper;

$speakV2Request = SpeakV2RequestBuilder::init(
    'text2'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

