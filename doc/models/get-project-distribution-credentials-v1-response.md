
# Get Project Distribution Credentials V1 Response

*This model accepts additional fields of type array.*

## Structure

`GetProjectDistributionCredentialsV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `member` | [`GetProjectDistributionCredentialsV1ResponseMember`](../../doc/models/get-project-distribution-credentials-v1-response-member.md) | Required | - | getMember(): GetProjectDistributionCredentialsV1ResponseMember | setMember(GetProjectDistributionCredentialsV1ResponseMember member): void |
| `distributionCredentials` | [`GetProjectDistributionCredentialsV1ResponseDistributionCredentials`](../../doc/models/get-project-distribution-credentials-v1-response-distribution-credentials.md) | Required | - | getDistributionCredentials(): GetProjectDistributionCredentialsV1ResponseDistributionCredentials | setDistributionCredentials(GetProjectDistributionCredentialsV1ResponseDistributionCredentials distributionCredentials): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\GetProjectDistributionCredentialsV1ResponseBuilder;
use DeepgramLib\Models\Builders\GetProjectDistributionCredentialsV1ResponseMemberBuilder;
use DeepgramLib\ApiHelper;
use DeepgramLib\Models\Builders\GetProjectDistributionCredentialsV1ResponseDistributionCredentialsBuilder;
use DeepgramLib\Utils\DateTimeHelper;

$getProjectDistributionCredentialsV1Response = GetProjectDistributionCredentialsV1ResponseBuilder::init(
    GetProjectDistributionCredentialsV1ResponseMemberBuilder::init(
        '00001922-0000-0000-0000-000000000000',
        'email0'
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    GetProjectDistributionCredentialsV1ResponseDistributionCredentialsBuilder::init(
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

