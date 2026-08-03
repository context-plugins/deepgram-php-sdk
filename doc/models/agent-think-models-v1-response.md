
# Agent Think Models V1 Response

*This model accepts additional fields of type array.*

## Structure

`AgentThinkModelsV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `models` | array<[AgentThinkModelsV1ResponseModelsItems0](../../doc/models/agent-think-models-v1-response-models-items-0.md)\|[AgentThinkModelsV1ResponseModelsItems1](../../doc/models/agent-think-models-v1-response-models-items-1.md)\|[AgentThinkModelsV1ResponseModelsItems2](../../doc/models/agent-think-models-v1-response-models-items-2.md)\|[AgentThinkModelsV1ResponseModelsItems3](../../doc/models/agent-think-models-v1-response-models-items-3.md)\|[AgentThinkModelsV1ResponseModelsItems4](../../doc/models/agent-think-models-v1-response-models-items-4.md)> | Required | - | getModels(): array | setModels(array models): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\AgentThinkModelsV1ResponseBuilder;
use RestApiLib\Models\Builders\AgentThinkModelsV1ResponseModelsItems0Builder;
use RestApiLib\Models\AgentThinkModelsV1ResponseModelsItemsOneOf0Id;
use RestApiLib\ApiHelper;

$agentThinkModelsV1Response = AgentThinkModelsV1ResponseBuilder::init(
    [
        AgentThinkModelsV1ResponseModelsItems0Builder::init(
            AgentThinkModelsV1ResponseModelsItemsOneOf0Id::GPT4O,
            'name0',
            ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ]
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

