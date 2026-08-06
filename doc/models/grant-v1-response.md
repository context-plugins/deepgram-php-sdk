
# Grant V1 Response

*This model accepts additional fields of type array.*

## Structure

`GrantV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accessToken` | `string` | Required | JSON Web Token (JWT) | getAccessToken(): string | setAccessToken(string accessToken): void |
| `expiresIn` | `?float` | Optional | Time in seconds until the JWT expires | getExpiresIn(): ?float | setExpiresIn(?float expiresIn): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\GrantV1ResponseBuilder;
use DeepgramLib\ApiHelper;

$grantV1Response = GrantV1ResponseBuilder::init(
    'access_token8'
)
    ->expiresIn(64.04)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

