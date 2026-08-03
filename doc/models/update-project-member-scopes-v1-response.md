
# Update Project Member Scopes V1 Response

*This model accepts additional fields of type array.*

## Structure

`UpdateProjectMemberScopesV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `message` | `?string` | Optional | confirmation message | getMessage(): ?string | setMessage(?string message): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\UpdateProjectMemberScopesV1ResponseBuilder;
use RestApiLib\ApiHelper;

$updateProjectMemberScopesV1Response = UpdateProjectMemberScopesV1ResponseBuilder::init()
    ->message('message0')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

