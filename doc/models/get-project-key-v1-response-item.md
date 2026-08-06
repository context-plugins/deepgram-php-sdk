
# Get Project Key V1 Response Item

*This model accepts additional fields of type array.*

## Structure

`GetProjectKeyV1ResponseItem`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `member` | [`?GetProjectKeyV1ResponseItemMember`](../../doc/models/get-project-key-v1-response-item-member.md) | Optional | - | getMember(): ?GetProjectKeyV1ResponseItemMember | setMember(?GetProjectKeyV1ResponseItemMember member): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\GetProjectKeyV1ResponseItemBuilder;
use DeepgramLib\Models\Builders\GetProjectKeyV1ResponseItemMemberBuilder;
use DeepgramLib\Models\Builders\GetProjectKeyV1ResponseItemMemberApiKeyBuilder;
use DeepgramLib\Utils\DateTimeHelper;
use DeepgramLib\ApiHelper;

$getProjectKeyV1ResponseItem = GetProjectKeyV1ResponseItemBuilder::init()
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
    ->build();
```

