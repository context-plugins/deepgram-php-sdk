
# List Project Keys V1 Response Api Keys Items Member

*This model accepts additional fields of type array.*

## Structure

`ListProjectKeysV1ResponseApiKeysItemsMember`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `memberId` | `?string` | Optional | - | getMemberId(): ?string | setMemberId(?string memberId): void |
| `email` | `?string` | Optional | - | getEmail(): ?string | setEmail(?string email): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListProjectKeysV1ResponseApiKeysItemsMemberBuilder;
use DeepgramLib\ApiHelper;

$listProjectKeysV1ResponseApiKeysItemsMember = ListProjectKeysV1ResponseApiKeysItemsMemberBuilder::init()
    ->memberId('member_id6')
    ->email('email0')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

