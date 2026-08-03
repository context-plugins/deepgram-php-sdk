
# List Project Members V1 Response Members Items

*This model accepts additional fields of type array.*

## Structure

`ListProjectMembersV1ResponseMembersItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `memberId` | `?string` | Optional | The unique identifier of the member | getMemberId(): ?string | setMemberId(?string memberId): void |
| `scopes` | `?(string[])` | Optional | The API scopes of the member | getScopes(): ?array | setScopes(?array scopes): void |
| `email` | `?string` | Optional | - | getEmail(): ?string | setEmail(?string email): void |
| `firstName` | `?string` | Optional | - | getFirstName(): ?string | setFirstName(?string firstName): void |
| `lastName` | `?string` | Optional | - | getLastName(): ?string | setLastName(?string lastName): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListProjectMembersV1ResponseMembersItemsBuilder;
use RestApiLib\ApiHelper;

$listProjectMembersV1ResponseMembersItems = ListProjectMembersV1ResponseMembersItemsBuilder::init()
    ->memberId('member_id0')
    ->scopes(
        [
            'scopes2',
            'scopes3'
        ]
    )
    ->email('email6')
    ->firstName('first_name0')
    ->lastName('last_name8')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

