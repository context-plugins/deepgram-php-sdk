
# Agent Think Models V1 Response Models Items 2

Google models

*This model accepts additional fields of type array.*

## Structure

`AgentThinkModelsV1ResponseModelsItems2`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | [`string(AgentThinkModelsV1ResponseModelsItemsOneOf2Id)`](../../doc/models/agent-think-models-v1-response-models-items-one-of-2-id.md) | Required | The unique identifier of the Google model | getId(): string | setId(string id): void |
| `name` | `string` | Required | The display name of the model | getName(): string | setName(string name): void |
| `provider` | `array` | Required | The provider of the model | getProvider(): array | setProvider(array provider): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\AgentThinkModelsV1ResponseModelsItems2Builder;
use DeepgramLib\Models\AgentThinkModelsV1ResponseModelsItemsOneOf2Id;
use DeepgramLib\ApiHelper;

$agentThinkModelsV1ResponseModelsItems2 = AgentThinkModelsV1ResponseModelsItems2Builder::init(
    AgentThinkModelsV1ResponseModelsItemsOneOf2Id::ENUM_GEMINI25FLASH,
    'name6',
    ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

