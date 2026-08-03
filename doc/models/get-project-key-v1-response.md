
# Get Project Key V1 Response

*This model accepts additional fields of type array.*

## Structure

`GetProjectKeyV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `item` | [`?GetProjectKeyV1ResponseItem`](../../doc/models/get-project-key-v1-response-item.md) | Optional | - | getItem(): ?GetProjectKeyV1ResponseItem | setItem(?GetProjectKeyV1ResponseItem item): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\GetProjectKeyV1ResponseBuilder;
use RestApiLib\Models\Builders\GetProjectKeyV1ResponseItemBuilder;
use RestApiLib\Models\Builders\GetProjectKeyV1ResponseItemMemberBuilder;
use RestApiLib\Models\Builders\GetProjectKeyV1ResponseItemMemberApiKeyBuilder;
use RestApiLib\Utils\DateTimeHelper;
use RestApiLib\ApiHelper;

$getProjectKeyV1Response = GetProjectKeyV1ResponseBuilder::init()
    ->item(
        GetProjectKeyV1ResponseItemBuilder::init()
            ->member(
                GetProjectKeyV1ResponseItemMemberBuilder::init()
                    ->memberId('member_id4')
                    ->email('email0')
                    ->firstName('first_name6')
                    ->lastName('last_name4')
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
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

