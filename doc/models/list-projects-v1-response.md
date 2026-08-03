
# List Projects V1 Response

*This model accepts additional fields of type array.*

## Structure

`ListProjectsV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `projects` | [`?(ListProjectsV1ResponseProjectsItems[])`](../../doc/models/list-projects-v1-response-projects-items.md) | Optional | - | getProjects(): ?array | setProjects(?array projects): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListProjectsV1ResponseBuilder;
use RestApiLib\Models\Builders\ListProjectsV1ResponseProjectsItemsBuilder;
use RestApiLib\ApiHelper;

$listProjectsV1Response = ListProjectsV1ResponseBuilder::init()
    ->projects(
        [
            ListProjectsV1ResponseProjectsItemsBuilder::init()
                ->projectId('project_id4')
                ->name('name2')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ListProjectsV1ResponseProjectsItemsBuilder::init()
                ->projectId('project_id4')
                ->name('name2')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

