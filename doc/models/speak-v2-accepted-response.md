
# Speak V2 Accepted Response

Accepted response returned when a callback URL is supplied; the audio is delivered asynchronously to that URL.

*This model accepts additional fields of type array.*

## Structure

`SpeakV2AcceptedResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `requestId` | `string` | Required | Unique identifier for tracking the asynchronous request | getRequestId(): string | setRequestId(string requestId): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\SpeakV2AcceptedResponseBuilder;
use RestApiLib\ApiHelper;

$speakV2AcceptedResponse = SpeakV2AcceptedResponseBuilder::init(
    '00001fa4-0000-0000-0000-000000000000'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

