
# Create Project Distribution Credentials V1 Request

Request body for creating distribution credentials

*This model accepts additional fields of type array.*

## Structure

`CreateProjectDistributionCredentialsV1Request`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `comment` | `?string` | Optional | Optional comment about the credentials | getComment(): ?string | setComment(?string comment): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\CreateProjectDistributionCredentialsV1RequestBuilder;
use RestApiLib\ApiHelper;

$createProjectDistributionCredentialsV1Request = CreateProjectDistributionCredentialsV1RequestBuilder::init()
    ->comment('comment2')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

