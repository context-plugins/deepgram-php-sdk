
# Listen V1 Accepted Response

Accepted response for asynchronous transcription requests

*This model accepts additional fields of type array.*

## Structure

`ListenV1AcceptedResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `requestId` | `string` | Required | Unique identifier for tracking the asynchronous request | getRequestId(): string | setRequestId(string requestId): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListenV1AcceptedResponseBuilder;
use DeepgramLib\ApiHelper;

$listenV1AcceptedResponse = ListenV1AcceptedResponseBuilder::init(
    '000016c8-0000-0000-0000-000000000000'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

