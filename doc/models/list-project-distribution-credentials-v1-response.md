
# List Project Distribution Credentials V1 Response

*This model accepts additional fields of type array.*

## Structure

`ListProjectDistributionCredentialsV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `distributionCredentials` | [`?(ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItems[])`](../../doc/models/list-project-distribution-credentials-v1-response-distribution-credentials-items.md) | Optional | Array of distribution credentials with associated member information | getDistributionCredentials(): ?array | setDistributionCredentials(?array distributionCredentials): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListProjectDistributionCredentialsV1ResponseBuilder;
use RestApiLib\Models\Builders\ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsBuilder;
use RestApiLib\Models\Builders\ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsMemberBuilder;
use RestApiLib\ApiHelper;
use RestApiLib\Models\Builders\ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsDistributionCredentialsBuilder;
use RestApiLib\Utils\DateTimeHelper;

$listProjectDistributionCredentialsV1Response = ListProjectDistributionCredentialsV1ResponseBuilder::init()
    ->distributionCredentials(
        [
            ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsBuilder::init(
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
                ->build(),
            ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsBuilder::init(
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
                ->build(),
            ListProjectDistributionCredentialsV1ResponseDistributionCredentialsItemsBuilder::init(
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
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

