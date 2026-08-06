
# Listen V1 Response Results Channels Items Alternatives Items Entities Items

*This model accepts additional fields of type array.*

## Structure

`ListenV1ResponseResultsChannelsItemsAlternativesItemsEntitiesItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `label` | `?string` | Optional | - | getLabel(): ?string | setLabel(?string label): void |
| `value` | `?string` | Optional | - | getValue(): ?string | setValue(?string value): void |
| `rawValue` | `?string` | Optional | - | getRawValue(): ?string | setRawValue(?string rawValue): void |
| `confidence` | `?float` | Optional | - | getConfidence(): ?float | setConfidence(?float confidence): void |
| `startWord` | `?float` | Optional | - | getStartWord(): ?float | setStartWord(?float startWord): void |
| `endWord` | `?float` | Optional | - | getEndWord(): ?float | setEndWord(?float endWord): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsAlternativesItemsEntitiesItemsBuilder;
use DeepgramLib\ApiHelper;

$listenV1ResponseResultsChannelsItemsAlternativesItemsEntitiesItems = ListenV1ResponseResultsChannelsItemsAlternativesItemsEntitiesItemsBuilder::init()
    ->label('label6')
    ->value('value8')
    ->rawValue('raw_value2')
    ->confidence(76.4)
    ->startWord(94.56)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

