
# Get Project Key V1 Response Item Member Api Key

*This model accepts additional fields of type array.*

## Structure

`GetProjectKeyV1ResponseItemMemberApiKey`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `apiKeyId` | `?string` | Optional | - | getApiKeyId(): ?string | setApiKeyId(?string apiKeyId): void |
| `comment` | `?string` | Optional | - | getComment(): ?string | setComment(?string comment): void |
| `scopes` | `?(string[])` | Optional | - | getScopes(): ?array | setScopes(?array scopes): void |
| `tags` | `?(string[])` | Optional | - | getTags(): ?array | setTags(?array tags): void |
| `expirationDate` | `?DateTime` | Optional | - | getExpirationDate(): ?\DateTime | setExpirationDate(?\DateTime expirationDate): void |
| `created` | `?DateTime` | Optional | - | getCreated(): ?\DateTime | setCreated(?\DateTime created): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\GetProjectKeyV1ResponseItemMemberApiKeyBuilder;
use RestApiLib\Utils\DateTimeHelper;
use RestApiLib\ApiHelper;

$getProjectKeyV1ResponseItemMemberApiKey = GetProjectKeyV1ResponseItemMemberApiKeyBuilder::init()
    ->apiKeyId('api_key_id4')
    ->comment('comment4')
    ->scopes(
        [
            'scopes8',
            'scopes7'
        ]
    )
    ->tags(
        [
            'tags5'
        ]
    )
    ->expirationDate(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

