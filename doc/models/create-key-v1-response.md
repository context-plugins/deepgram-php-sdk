
# Create Key V1 Response

API key created

*This model accepts additional fields of type array.*

## Structure

`CreateKeyV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `apiKeyId` | `?string` | Optional | The unique identifier of the API key | getApiKeyId(): ?string | setApiKeyId(?string apiKeyId): void |
| `key` | `?string` | Optional | The API key | getKey(): ?string | setKey(?string key): void |
| `comment` | `?string` | Optional | A comment for the API key | getComment(): ?string | setComment(?string comment): void |
| `scopes` | `?(string[])` | Optional | The scopes for the API key | getScopes(): ?array | setScopes(?array scopes): void |
| `tags` | `?(string[])` | Optional | The tags for the API key | getTags(): ?array | setTags(?array tags): void |
| `expirationDate` | `?DateTime` | Optional | The expiration date of the API key | getExpirationDate(): ?\DateTime | setExpirationDate(?\DateTime expirationDate): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\CreateKeyV1ResponseBuilder;
use RestApiLib\ApiHelper;

$createKeyV1Response = CreateKeyV1ResponseBuilder::init()
    ->apiKeyId('api_key_id0')
    ->key('key6')
    ->comment('comment0')
    ->scopes(
        [
            'scopes6',
            'scopes7',
            'scopes8'
        ]
    )
    ->tags(
        [
            'tags1',
            'tags2',
            'tags3'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

