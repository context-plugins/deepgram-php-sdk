
# Create Project Distribution Credentials V1 Response

*This model accepts additional fields of type array.*

## Structure

`CreateProjectDistributionCredentialsV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `member` | [`CreateProjectDistributionCredentialsV1ResponseMember`](../../doc/models/create-project-distribution-credentials-v1-response-member.md) | Required | - | getMember(): CreateProjectDistributionCredentialsV1ResponseMember | setMember(CreateProjectDistributionCredentialsV1ResponseMember member): void |
| `distributionCredentials` | [`CreateProjectDistributionCredentialsV1ResponseDistributionCredentials`](../../doc/models/create-project-distribution-credentials-v1-response-distribution-credentials.md) | Required | - | getDistributionCredentials(): CreateProjectDistributionCredentialsV1ResponseDistributionCredentials | setDistributionCredentials(CreateProjectDistributionCredentialsV1ResponseDistributionCredentials distributionCredentials): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\CreateProjectDistributionCredentialsV1ResponseBuilder;
use RestApiLib\Models\Builders\CreateProjectDistributionCredentialsV1ResponseMemberBuilder;
use RestApiLib\ApiHelper;
use RestApiLib\Models\Builders\CreateProjectDistributionCredentialsV1ResponseDistributionCredentialsBuilder;
use RestApiLib\Utils\DateTimeHelper;

$createProjectDistributionCredentialsV1Response = CreateProjectDistributionCredentialsV1ResponseBuilder::init(
    CreateProjectDistributionCredentialsV1ResponseMemberBuilder::init(
        '00001922-0000-0000-0000-000000000000',
        'email0'
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    CreateProjectDistributionCredentialsV1ResponseDistributionCredentialsBuilder::init(
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

