
# Read V1 Request Url

*This model accepts additional fields of type array.*

## Structure

`ReadV1RequestUrl`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `url` | `string` | Required | A URL pointing to the text source | getUrl(): string | setUrl(string url): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ReadV1RequestUrlBuilder;
use RestApiLib\ApiHelper;

$readV1RequestUrl = ReadV1RequestUrlBuilder::init(
    'url2'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

