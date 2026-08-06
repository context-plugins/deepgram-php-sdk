
# List Project Distribution Credentials V1 Response Distribution Credentials Items Distribution Credentials

*This model accepts additional fields of type array.*

## Structure

`ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsDistributionCredentials`

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
use DeepgramLib\Models\Builders\ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsDistributionCredentialsBuilder;
use DeepgramLib\Utils\DateTimeHelper;
use DeepgramLib\ApiHelper;

$listProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsDistributionCredentials = ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsDistributionCredentialsBuilder::init(
    '000022fe-0000-0000-0000-000000000000',
    'provider6',
    [
        'scopes0',
        'scopes1'
    ],
    DateTimeHelper::fromRfc3339DateTimeRequired('2016-03-13T12:52:32.123Z')
)
    ->comment('comment4')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

