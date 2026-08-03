
# List Agent Variables V1 Response

*This model accepts additional fields of type array.*

## Structure

`ListAgentVariablesV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `variables` | [`?(AgentVariableV1[])`](../../doc/models/agent-variable-v1.md) | Optional | A list of agent variables for the project | getVariables(): ?array | setVariables(?array variables): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListAgentVariablesV1ResponseBuilder;
use RestApiLib\Models\Builders\AgentVariableV1Builder;
use RestApiLib\ApiHelper;
use RestApiLib\Utils\DateTimeHelper;

$listAgentVariablesV1Response = ListAgentVariablesV1ResponseBuilder::init()
    ->variables(
        [
            AgentVariableV1Builder::init(
                'variable_id6',
                'key2',
                ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
            )
                ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

