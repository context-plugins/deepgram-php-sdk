
# List Projects V1 Response Projects Items

*This model accepts additional fields of type array.*

## Structure

`ListProjectsV1ResponseProjectsItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `projectId` | `?string` | Optional | The unique identifier of the project | getProjectId(): ?string | setProjectId(?string projectId): void |
| `name` | `?string` | Optional | The name of the project | getName(): ?string | setName(?string name): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListProjectsV1ResponseProjectsItemsBuilder;
use RestApiLib\ApiHelper;

$listProjectsV1ResponseProjectsItems = ListProjectsV1ResponseProjectsItemsBuilder::init()
    ->projectId('project_id4')
    ->name('name2')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

