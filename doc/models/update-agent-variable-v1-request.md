
# Update Agent Variable V1 Request

Request body for updating an agent variable

*This model accepts additional fields of type array.*

## Structure

`UpdateAgentVariableV1Request`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `value` | `array` | Required | The new value to substitute | getValue(): array | setValue(array value): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\UpdateAgentVariableV1RequestBuilder;
use DeepgramLib\ApiHelper;

$updateAgentVariableV1Request = UpdateAgentVariableV1RequestBuilder::init(
    ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

