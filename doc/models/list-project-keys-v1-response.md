
# List Project Keys V1 Response

*This model accepts additional fields of type array.*

## Structure

`ListProjectKeysV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `apiKeys` | [`?(ListProjectKeysV1ResponseApiKeysItems[])`](../../doc/models/list-project-keys-v1-response-api-keys-items.md) | Optional | - | getApiKeys(): ?array | setApiKeys(?array apiKeys): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListProjectKeysV1ResponseBuilder;
use RestApiLib\Models\Builders\ListProjectKeysV1ResponseApiKeysItemsBuilder;
use RestApiLib\Models\Builders\ListProjectKeysV1ResponseApiKeysItemsMemberBuilder;
use RestApiLib\ApiHelper;
use RestApiLib\Models\Builders\ListProjectKeysV1ResponseApiKeysItemsApiKeyBuilder;
use RestApiLib\Utils\DateTimeHelper;

$listProjectKeysV1Response = ListProjectKeysV1ResponseBuilder::init()
    ->apiKeys(
        [
            ListProjectKeysV1ResponseApiKeysItemsBuilder::init()
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
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

