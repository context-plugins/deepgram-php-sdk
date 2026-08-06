
# List Project Keys V1 Response Api Keys Items Api Key

*This model accepts additional fields of type array.*

## Structure

`ListProjectKeysV1ResponseApiKeysItemsApiKey`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `apiKeyId` | `?string` | Optional | - | getApiKeyId(): ?string | setApiKeyId(?string apiKeyId): void |
| `comment` | `?string` | Optional | - | getComment(): ?string | setComment(?string comment): void |
| `scopes` | `?(string[])` | Optional | - | getScopes(): ?array | setScopes(?array scopes): void |
| `created` | `?DateTime` | Optional | - | getCreated(): ?\DateTime | setCreated(?\DateTime created): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListProjectKeysV1ResponseApiKeysItemsApiKeyBuilder;
use DeepgramLib\Utils\DateTimeHelper;
use DeepgramLib\ApiHelper;

$listProjectKeysV1ResponseApiKeysItemsApiKey = ListProjectKeysV1ResponseApiKeysItemsApiKeyBuilder::init()
    ->apiKeyId('api_key_id8')
    ->comment('comment2')
    ->scopes(
        [
            'scopes8',
            'scopes9',
            'scopes0'
        ]
    )
    ->created(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

