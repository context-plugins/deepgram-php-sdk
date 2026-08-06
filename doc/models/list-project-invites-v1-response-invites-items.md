
# List Project Invites V1 Response Invites Items

*This model accepts additional fields of type array.*

## Structure

`ListProjectInvitesV1ResponseInvitesItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `email` | `?string` | Optional | The email address of the invitee | getEmail(): ?string | setEmail(?string email): void |
| `scope` | `?string` | Optional | The scope of the invitee | getScope(): ?string | setScope(?string scope): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListProjectInvitesV1ResponseInvitesItemsBuilder;
use DeepgramLib\ApiHelper;

$listProjectInvitesV1ResponseInvitesItems = ListProjectInvitesV1ResponseInvitesItemsBuilder::init()
    ->email('email4')
    ->scope('scope0')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

