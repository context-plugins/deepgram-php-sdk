
# List Models V1 Response Tts Models Metadata

*This model accepts additional fields of type array.*

## Structure

`ListModelsV1ResponseTtsModelsMetadata`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accent` | `?string` | Optional | - | getAccent(): ?string | setAccent(?string accent): void |
| `age` | `?string` | Optional | - | getAge(): ?string | setAge(?string age): void |
| `color` | `?string` | Optional | - | getColor(): ?string | setColor(?string color): void |
| `image` | `?string` | Optional | - | getImage(): ?string | setImage(?string image): void |
| `sample` | `?string` | Optional | - | getSample(): ?string | setSample(?string sample): void |
| `tags` | `?(string[])` | Optional | - | getTags(): ?array | setTags(?array tags): void |
| `useCases` | `?(string[])` | Optional | - | getUseCases(): ?array | setUseCases(?array useCases): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListModelsV1ResponseTtsModelsMetadataBuilder;
use RestApiLib\ApiHelper;

$listModelsV1ResponseTtsModelsMetadata = ListModelsV1ResponseTtsModelsMetadataBuilder::init()
    ->accent('accent4')
    ->age('age8')
    ->color('color4')
    ->image('image6')
    ->sample('sample8')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

