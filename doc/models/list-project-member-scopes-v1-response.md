
# List Project Member Scopes V1 Response

*This model accepts additional fields of type array.*

## Structure

`ListProjectMemberScopesV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `scopes` | `?(string[])` | Optional | The API scopes of the member | getScopes(): ?array | setScopes(?array scopes): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListProjectMemberScopesV1ResponseBuilder;
use RestApiLib\ApiHelper;

$listProjectMemberScopesV1Response = ListProjectMemberScopesV1ResponseBuilder::init()
    ->scopes(
        [
            'scopes4',
            'scopes3'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

