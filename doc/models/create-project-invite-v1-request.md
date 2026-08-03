
# Create Project Invite V1 Request

Request body for creating a project invite

*This model accepts additional fields of type array.*

## Structure

`CreateProjectInviteV1Request`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `email` | `string` | Required | The email address of the invitee | getEmail(): string | setEmail(string email): void |
| `scope` | `string` | Required | The scope of the invitee | getScope(): string | setScope(string scope): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\CreateProjectInviteV1RequestBuilder;
use RestApiLib\ApiHelper;

$createProjectInviteV1Request = CreateProjectInviteV1RequestBuilder::init(
    'email6',
    'scope2'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

