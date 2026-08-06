
# Create Agent Variable V1 Request

Request body for creating an agent variable

*This model accepts additional fields of type array.*

## Structure

`CreateAgentVariableV1Request`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `key` | `string` | Required | The variable name, following the DG_<VARIABLE_NAME> format | getKey(): string | setKey(string key): void |
| `value` | `array` | Required | The value to substitute. Can be any valid JSON type (string, number, boolean, object, or array) | getValue(): array | setValue(array value): void |
| `apiVersion` | `?int` | Optional | API version. Defaults to 1<br><br>**Default**: `1` | getApiVersion(): ?int | setApiVersion(?int apiVersion): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\CreateAgentVariableV1RequestBuilder;
use DeepgramLib\ApiHelper;

$createAgentVariableV1Request = CreateAgentVariableV1RequestBuilder::init(
    'key0',
    ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
)
    ->apiVersion(1)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

