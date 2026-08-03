
# Agent Think Models V1 Response Models Items 1

Anthropic models

*This model accepts additional fields of type array.*

## Structure

`AgentThinkModelsV1ResponseModelsItems1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | [`string(AgentThinkModelsV1ResponseModelsItemsOneOf1Id)`](../../doc/models/agent-think-models-v1-response-models-items-one-of-1-id.md) | Required | The unique identifier of the Anthropic model | getId(): string | setId(string id): void |
| `name` | `string` | Required | The display name of the model | getName(): string | setName(string name): void |
| `provider` | `array` | Required | The provider of the model | getProvider(): array | setProvider(array provider): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\AgentThinkModelsV1ResponseModelsItems1Builder;
use RestApiLib\Models\AgentThinkModelsV1ResponseModelsItemsOneOf1Id;
use RestApiLib\ApiHelper;

$agentThinkModelsV1ResponseModelsItems1 = AgentThinkModelsV1ResponseModelsItems1Builder::init(
    AgentThinkModelsV1ResponseModelsItemsOneOf1Id::CLAUDE35HAIKULATEST,
    'name2',
    ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

