
# Agent Think Models V1 Response Models Items 0

OpenAI models

*This model accepts additional fields of type array.*

## Structure

`AgentThinkModelsV1ResponseModelsItems0`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | [`string(AgentThinkModelsV1ResponseModelsItemsOneOf0Id)`](../../doc/models/agent-think-models-v1-response-models-items-one-of-0-id.md) | Required | The unique identifier of the OpenAI model | getId(): string | setId(string id): void |
| `name` | `string` | Required | The display name of the model | getName(): string | setName(string name): void |
| `provider` | `array` | Required | The provider of the model | getProvider(): array | setProvider(array provider): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\AgentThinkModelsV1ResponseModelsItems0Builder;
use RestApiLib\Models\AgentThinkModelsV1ResponseModelsItemsOneOf0Id;
use RestApiLib\ApiHelper;

$agentThinkModelsV1ResponseModelsItems0 = AgentThinkModelsV1ResponseModelsItems0Builder::init(
    AgentThinkModelsV1ResponseModelsItemsOneOf0Id::ENUM_GPT41MINI,
    'name0',
    ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

