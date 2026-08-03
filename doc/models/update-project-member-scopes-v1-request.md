
# Update Project Member Scopes V1 Request

*This model accepts additional fields of type array.*

## Structure

`UpdateProjectMemberScopesV1Request`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `scope` | `string` | Required | A scope to update | getScope(): string | setScope(string scope): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\UpdateProjectMemberScopesV1RequestBuilder;
use RestApiLib\ApiHelper;

$updateProjectMemberScopesV1Request = UpdateProjectMemberScopesV1RequestBuilder::init(
    'scope0'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

