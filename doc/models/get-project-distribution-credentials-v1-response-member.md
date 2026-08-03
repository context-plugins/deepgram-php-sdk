
# Get Project Distribution Credentials V1 Response Member

*This model accepts additional fields of type array.*

## Structure

`GetProjectDistributionCredentialsV1ResponseMember`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `memberId` | `string` | Required | Unique identifier for the member | getMemberId(): string | setMemberId(string memberId): void |
| `email` | `string` | Required | Email address of the member | getEmail(): string | setEmail(string email): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\GetProjectDistributionCredentialsV1ResponseMemberBuilder;
use RestApiLib\ApiHelper;

$getProjectDistributionCredentialsV1ResponseMember = GetProjectDistributionCredentialsV1ResponseMemberBuilder::init(
    '00000eba-0000-0000-0000-000000000000',
    'email6'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

