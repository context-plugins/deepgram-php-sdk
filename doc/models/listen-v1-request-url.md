
# Listen V1 Request Url

Audio file URL to transcribe

*This model accepts additional fields of type array.*

## Structure

`ListenV1RequestUrl`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `url` | `string` | Required | - | getUrl(): string | setUrl(string url): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListenV1RequestUrlBuilder;
use DeepgramLib\ApiHelper;

$listenV1RequestUrl = ListenV1RequestUrlBuilder::init(
    'url8'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

