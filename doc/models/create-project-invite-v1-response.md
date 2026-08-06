
# Create Project Invite V1 Response

*This model accepts additional fields of type array.*

## Structure

`CreateProjectInviteV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `message` | `?string` | Optional | confirmation message | getMessage(): ?string | setMessage(?string message): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\CreateProjectInviteV1ResponseBuilder;
use DeepgramLib\ApiHelper;

$createProjectInviteV1Response = CreateProjectInviteV1ResponseBuilder::init()
    ->message('message4')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

