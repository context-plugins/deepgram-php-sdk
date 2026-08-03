
# List Project Distribution Credentials V1 Response Distribution Credentials Items

*This model accepts additional fields of type array.*

## Structure

`ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `member` | [`ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsMember`](../../doc/models/list-project-distribution-credentials-v1-response-distribution-credentials-items-member.md) | Required | - | getMember(): ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsMember | setMember(ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsMember member): void |
| `distributionCredentials` | [`ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsDistributionCredentials`](../../doc/models/list-project-distribution-credentials-v1-response-distribution-credentials-items-distribution-credentials.md) | Required | - | getDistributionCredentials(): ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsDistributionCredentials | setDistributionCredentials(ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsDistributionCredentials distributionCredentials): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsBuilder;
use RestApiLib\Models\Builders\ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsMemberBuilder;
use RestApiLib\ApiHelper;
use RestApiLib\Models\Builders\ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsDistributionCredentialsBuilder;
use RestApiLib\Utils\DateTimeHelper;

$listProjectDistributionCredentialsV1ResponseDistributionCredentialsItems = ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsBuilder::init(
    ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsMemberBuilder::init(
        '00001922-0000-0000-0000-000000000000',
        'email0'
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsDistributionCredentialsBuilder::init(
        '00000560-0000-0000-0000-000000000000',
        'provider4',
        [
            'scopes8',
            'scopes9'
        ],
        DateTimeHelper::fromRfc3339DateTimeRequired('2016-03-13T12:52:32.123Z')
    )
        ->comment('comment2')
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

