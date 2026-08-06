
# List Project Distribution Credentials V1 Response Distribution Credentials Items Member

*This model accepts additional fields of type array.*

## Structure

`ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsMember`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `memberId` | `string` | Required | Unique identifier for the member | getMemberId(): string | setMemberId(string memberId): void |
| `email` | `string` | Required | Email address of the member | getEmail(): string | setEmail(string email): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsMemberBuilder;
use DeepgramLib\ApiHelper;

$listProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsMember = ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsMemberBuilder::init(
    '0000062e-0000-0000-0000-000000000000',
    'email4'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

