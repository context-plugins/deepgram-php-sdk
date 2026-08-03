
# Agent Think Models V1 Response Models Items 4

AWS Bedrock models (custom models accepted)

*This model accepts additional fields of type array.*

## Structure

`AgentThinkModelsV1ResponseModelsItems4`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `string` | Required | The unique identifier of the AWS Bedrock model (any model string accepted for BYO LLMs) | getId(): string | setId(string id): void |
| `name` | `string` | Required | The display name of the model | getName(): string | setName(string name): void |
| `provider` | `array` | Required | The provider of the model | getProvider(): array | setProvider(array provider): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\AgentThinkModelsV1ResponseModelsItems4Builder;
use RestApiLib\ApiHelper;

$agentThinkModelsV1ResponseModelsItems4 = AgentThinkModelsV1ResponseModelsItems4Builder::init(
    'id0',
    'name0',
    ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

