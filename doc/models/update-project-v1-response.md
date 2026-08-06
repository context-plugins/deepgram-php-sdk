
# Update Project V1 Response

*This model accepts additional fields of type array.*

## Structure

`UpdateProjectV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `message` | `?string` | Optional | confirmation message | getMessage(): ?string | setMessage(?string message): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\UpdateProjectV1ResponseBuilder;
use DeepgramLib\ApiHelper;

$updateProjectV1Response = UpdateProjectV1ResponseBuilder::init()
    ->message('message6')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

