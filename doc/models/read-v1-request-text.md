
# Read V1 Request Text

*This model accepts additional fields of type array.*

## Structure

`ReadV1RequestText`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `text` | `string` | Required | The plain text to analyze | getText(): string | setText(string text): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ReadV1RequestTextBuilder;
use DeepgramLib\ApiHelper;

$readV1RequestText = ReadV1RequestTextBuilder::init(
    'text0'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

