
# Create Project Distribution Credentials V1 Response Distribution Credentials

*This model accepts additional fields of type array.*

## Structure

`CreateProjectDistributionCredentialsV1ResponseDistributionCredentials`

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
use RestApiLib\Models\Builders\CreateProjectDistributionCredentialsV1ResponseDistributionCredentialsBuilder;
use RestApiLib\Utils\DateTimeHelper;
use RestApiLib\ApiHelper;

$createProjectDistributionCredentialsV1ResponseDistributionCredentials = CreateProjectDistributionCredentialsV1ResponseDistributionCredentialsBuilder::init(
    '000002fc-0000-0000-0000-000000000000',
    'provider2',
    [
        'scopes6',
        'scopes7'
    ],
    DateTimeHelper::fromRfc3339DateTimeRequired('2016-03-13T12:52:32.123Z')
)
    ->comment('comment0')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

