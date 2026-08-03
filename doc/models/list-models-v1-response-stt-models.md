
# List Models V1 Response Stt Models

*This model accepts additional fields of type array.*

## Structure

`ListModelsV1ResponseSttModels`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | - | getName(): ?string | setName(?string name): void |
| `canonicalName` | `?string` | Optional | - | getCanonicalName(): ?string | setCanonicalName(?string canonicalName): void |
| `architecture` | `?string` | Optional | - | getArchitecture(): ?string | setArchitecture(?string architecture): void |
| `languages` | `?(string[])` | Optional | - | getLanguages(): ?array | setLanguages(?array languages): void |
| `version` | `?string` | Optional | - | getVersion(): ?string | setVersion(?string version): void |
| `uuid` | `?string` | Optional | - | getUuid(): ?string | setUuid(?string uuid): void |
| `batch` | `?bool` | Optional | - | getBatch(): ?bool | setBatch(?bool batch): void |
| `streaming` | `?bool` | Optional | - | getStreaming(): ?bool | setStreaming(?bool streaming): void |
| `formattedOutput` | `?bool` | Optional | - | getFormattedOutput(): ?bool | setFormattedOutput(?bool formattedOutput): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListModelsV1ResponseSttModelsBuilder;
use RestApiLib\ApiHelper;

$listModelsV1ResponseSttModels = ListModelsV1ResponseSttModelsBuilder::init()
    ->name('name8')
    ->canonicalName('canonical_name6')
    ->architecture('architecture6')
    ->languages(
        [
            'languages5',
            'languages6',
            'languages7'
        ]
    )
    ->version('version4')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

