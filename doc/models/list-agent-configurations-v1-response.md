
# List Agent Configurations V1 Response

*This model accepts additional fields of type array.*

## Structure

`ListAgentConfigurationsV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `agents` | [`?(AgentConfigurationV1[])`](../../doc/models/agent-configuration-v1.md) | Optional | A list of agent configurations for the project | getAgents(): ?array | setAgents(?array agents): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListAgentConfigurationsV1ResponseBuilder;
use DeepgramLib\Models\Builders\AgentConfigurationV1Builder;
use DeepgramLib\ApiHelper;
use DeepgramLib\Utils\DateTimeHelper;

$listAgentConfigurationsV1Response = ListAgentConfigurationsV1ResponseBuilder::init()
    ->agents(
        [
            AgentConfigurationV1Builder::init(
                'agent_id8',
                ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
            )
                ->metadata(
                    [
                        'key0' => 'metadata3',
                        'key1' => 'metadata4'
                    ]
                )
                ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            AgentConfigurationV1Builder::init(
                'agent_id8',
                ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
            )
                ->metadata(
                    [
                        'key0' => 'metadata3',
                        'key1' => 'metadata4'
                    ]
                )
                ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            AgentConfigurationV1Builder::init(
                'agent_id8',
                ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
            )
                ->metadata(
                    [
                        'key0' => 'metadata3',
                        'key1' => 'metadata4'
                    ]
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

