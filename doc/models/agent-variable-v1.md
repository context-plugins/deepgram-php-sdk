
# Agent Variable V1

A template variable for agent configurations

*This model accepts additional fields of type array.*

## Structure

`AgentVariableV1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `variableId` | `string` | Required | The unique identifier of the variable | getVariableId(): string | setVariableId(string variableId): void |
| `key` | `string` | Required | The variable name, following the DG_<VARIABLE_NAME> format | getKey(): string | setKey(string key): void |
| `value` | `array` | Required | The value to substitute. Can be any valid JSON type | getValue(): array | setValue(array value): void |
| `createdAt` | `?DateTime` | Optional | Timestamp when the variable was created | getCreatedAt(): ?\DateTime | setCreatedAt(?\DateTime createdAt): void |
| `updatedAt` | `?DateTime` | Optional | Timestamp when the variable was last updated | getUpdatedAt(): ?\DateTime | setUpdatedAt(?\DateTime updatedAt): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\AgentVariableV1Builder;
use DeepgramLib\ApiHelper;
use DeepgramLib\Utils\DateTimeHelper;

$agentVariableV1 = AgentVariableV1Builder::init(
    'variable_id6',
    'key2',
    ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
)
    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

