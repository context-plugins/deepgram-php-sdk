
# Create Agent Configuration V1 Response

*This model accepts additional fields of type array.*

## Structure

`CreateAgentConfigurationV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `agentId` | `string` | Required | The unique identifier of the newly created agent configuration | getAgentId(): string | setAgentId(string agentId): void |
| `config` | `array` | Required | The parsed agent configuration object | getConfig(): array | setConfig(array config): void |
| `metadata` | `?array<string,string>` | Optional | Metadata associated with the agent configuration | getMetadata(): ?array | setMetadata(?array metadata): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\CreateAgentConfigurationV1ResponseBuilder;
use RestApiLib\ApiHelper;

$createAgentConfigurationV1Response = CreateAgentConfigurationV1ResponseBuilder::init(
    'agent_id6',
    ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
)
    ->metadata(
        [
            'key0' => 'metadata5',
            'key1' => 'metadata4'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

