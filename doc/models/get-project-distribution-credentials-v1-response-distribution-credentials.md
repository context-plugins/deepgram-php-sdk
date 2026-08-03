
# Get Project Distribution Credentials V1 Response Distribution Credentials

*This model accepts additional fields of type array.*

## Structure

`GetProjectDistributionCredentialsV1ResponseDistributionCredentials`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `distributionCredentialsId` | `string` | Required | Unique identifier for the distribution credentials | getDistributionCredentialsId(): string | setDistributionCredentialsId(string distributionCredentialsId): void |
| `provider` | `string` | Required | The provider of the distribution service | getProvider(): string | setProvider(string provider): void |
| `comment` | `?string` | Optional | Optional comment about the credentials | getComment(): ?string | setComment(?string comment): void |
| `scopes` | `string[]` | Required | List of permission scopes for the credentials | getScopes(): array | setScopes(array scopes): void |
| `created` | `DateTime` | Required | Timestamp when the credentials were created | getCreated(): \DateTime | setCreated(\DateTime created): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\GetProjectDistributionCredentialsV1ResponseDistributionCredentialsBuilder;
use RestApiLib\Utils\DateTimeHelper;
use RestApiLib\ApiHelper;

$getProjectDistributionCredentialsV1ResponseDistributionCredentials = GetProjectDistributionCredentialsV1ResponseDistributionCredentialsBuilder::init(
    '00001798-0000-0000-0000-000000000000',
    'provider8',
    [
        'scopes8'
    ],
    DateTimeHelper::fromRfc3339DateTimeRequired('2016-03-13T12:52:32.123Z')
)
    ->comment('comment4')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

