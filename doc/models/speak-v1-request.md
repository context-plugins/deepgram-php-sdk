
# Speak V1 Request

Request body for text-to-speech conversion

*This model accepts additional fields of type array.*

## Structure

`SpeakV1Request`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `text` | `string` | Required | The text content to be converted to speech | getText(): string | setText(string text): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\SpeakV1RequestBuilder;
use RestApiLib\ApiHelper;

$speakV1Request = SpeakV1RequestBuilder::init(
    'text2'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

