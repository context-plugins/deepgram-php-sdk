
# Update Project V1 Request

*This model accepts additional fields of type array.*

## Structure

`UpdateProjectV1Request`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | The name of the project | getName(): ?string | setName(?string name): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\UpdateProjectV1RequestBuilder;
use DeepgramLib\ApiHelper;

$updateProjectV1Request = UpdateProjectV1RequestBuilder::init()
    ->name('name2')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

