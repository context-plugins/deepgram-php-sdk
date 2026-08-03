
# Get Project Key V1 Response Item Member

*This model accepts additional fields of type array.*

## Structure

`GetProjectKeyV1ResponseItemMember`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `memberId` | `?string` | Optional | - | getMemberId(): ?string | setMemberId(?string memberId): void |
| `email` | `?string` | Optional | - | getEmail(): ?string | setEmail(?string email): void |
| `firstName` | `?string` | Optional | - | getFirstName(): ?string | setFirstName(?string firstName): void |
| `lastName` | `?string` | Optional | - | getLastName(): ?string | setLastName(?string lastName): void |
| `apiKey` | [`?GetProjectKeyV1ResponseItemMemberApiKey`](../../doc/models/get-project-key-v1-response-item-member-api-key.md) | Optional | - | getApiKey(): ?GetProjectKeyV1ResponseItemMemberApiKey | setApiKey(?GetProjectKeyV1ResponseItemMemberApiKey apiKey): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\GetProjectKeyV1ResponseItemMemberBuilder;
use RestApiLib\Models\Builders\GetProjectKeyV1ResponseItemMemberApiKeyBuilder;
use RestApiLib\Utils\DateTimeHelper;
use RestApiLib\ApiHelper;

$getProjectKeyV1ResponseItemMember = GetProjectKeyV1ResponseItemMemberBuilder::init()
    ->memberId('member_id0')
    ->email('email6')
    ->firstName('first_name0')
    ->lastName('last_name8')
    ->apiKey(
        GetProjectKeyV1ResponseItemMemberApiKeyBuilder::init()
            ->apiKeyId('api_key_id6')
            ->comment('comment6')
            ->scopes(
                [
                    'scopes4',
                    'scopes3'
                ]
            )
            ->tags(
                [
                    'tags7',
                    'tags8',
                    'tags9'
                ]
            )
            ->expirationDate(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

