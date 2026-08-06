
# Agent Configuration V1

A reusable agent configuration

*This model accepts additional fields of type array.*

## Structure

`AgentConfigurationV1`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `agentId` | `string` | Required | The unique identifier of the agent configuration | getAgentId(): string | setAgentId(string agentId): void |
| `config` | `array` | Required | The agent configuration object | getConfig(): array | setConfig(array config): void |
| `metadata` | `?array<string,string>` | Optional | A map of arbitrary key-value pairs for labeling or organizing the agent configuration | getMetadata(): ?array | setMetadata(?array metadata): void |
| `createdAt` | `?DateTime` | Optional | Timestamp when the configuration was created | getCreatedAt(): ?\DateTime | setCreatedAt(?\DateTime createdAt): void |
| `updatedAt` | `?DateTime` | Optional | Timestamp when the configuration was last updated | getUpdatedAt(): ?\DateTime | setUpdatedAt(?\DateTime updatedAt): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\AgentConfigurationV1Builder;
use DeepgramLib\ApiHelper;
use DeepgramLib\Utils\DateTimeHelper;

$agentConfigurationV1 = AgentConfigurationV1Builder::init(
    'agent_id0',
    ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
)
    ->metadata(
        [
            'key0' => 'metadata9',
            'key1' => 'metadata8'
        ]
    )
    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

