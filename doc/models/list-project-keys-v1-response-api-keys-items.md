
# List Project Keys V1 Response Api Keys Items

*This model accepts additional fields of type array.*

## Structure

`ListProjectKeysV1ResponseApiKeysItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `member` | [`?ListProjectKeysV1ResponseApiKeysItemsMember`](../../doc/models/list-project-keys-v1-response-api-keys-items-member.md) | Optional | - | getMember(): ?ListProjectKeysV1ResponseApiKeysItemsMember | setMember(?ListProjectKeysV1ResponseApiKeysItemsMember member): void |
| `apiKey` | [`?ListProjectKeysV1ResponseApiKeysItemsApiKey`](../../doc/models/list-project-keys-v1-response-api-keys-items-api-key.md) | Optional | - | getApiKey(): ?ListProjectKeysV1ResponseApiKeysItemsApiKey | setApiKey(?ListProjectKeysV1ResponseApiKeysItemsApiKey apiKey): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListProjectKeysV1ResponseApiKeysItemsBuilder;
use DeepgramLib\Models\Builders\ListProjectKeysV1ResponseApiKeysItemsMemberBuilder;
use DeepgramLib\ApiHelper;
use DeepgramLib\Models\Builders\ListProjectKeysV1ResponseApiKeysItemsApiKeyBuilder;
use DeepgramLib\Utils\DateTimeHelper;

$listProjectKeysV1ResponseApiKeysItems = ListProjectKeysV1ResponseApiKeysItemsBuilder::init()
    ->member(
        ListProjectKeysV1ResponseApiKeysItemsMemberBuilder::init()
            ->memberId('member_id4')
            ->email('email0')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->apiKey(
        ListProjectKeysV1ResponseApiKeysItemsApiKeyBuilder::init()
            ->apiKeyId('api_key_id6')
            ->comment('comment6')
            ->scopes(
                [
                    'scopes4',
                    'scopes3'
                ]
            )
            ->created(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

