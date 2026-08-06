
# Get Project V1 Response

*This model accepts additional fields of type array.*

## Structure

`GetProjectV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `projectId` | `?string` | Optional | The unique identifier of the project | getProjectId(): ?string | setProjectId(?string projectId): void |
| `mipOptOut` | `?bool` | Optional | Model Improvement Program opt-out | getMipOptOut(): ?bool | setMipOptOut(?bool mipOptOut): void |
| `name` | `?string` | Optional | The name of the project | getName(): ?string | setName(?string name): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\GetProjectV1ResponseBuilder;
use DeepgramLib\ApiHelper;

$getProjectV1Response = GetProjectV1ResponseBuilder::init()
    ->projectId('project_id8')
    ->mipOptOut(false)
    ->name('name8')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

