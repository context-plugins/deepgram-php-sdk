
# Grant V1 Request

*This model accepts additional fields of type array.*

## Structure

`GrantV1Request`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ttlSeconds` | `?float` | Optional | Time to live in seconds for the token. Defaults to 30 seconds. | getTtlSeconds(): ?float | setTtlSeconds(?float ttlSeconds): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\GrantV1RequestBuilder;
use RestApiLib\ApiHelper;

$grantV1Request = GrantV1RequestBuilder::init()
    ->ttlSeconds(33.48)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

