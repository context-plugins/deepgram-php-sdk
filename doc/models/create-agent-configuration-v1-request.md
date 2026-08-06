
# Create Agent Configuration V1 Request

Request body for creating an agent configuration

*This model accepts additional fields of type array.*

## Structure

`CreateAgentConfigurationV1Request`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `config` | `string` | Required | A valid JSON string representing the agent block of a Settings message | getConfig(): string | setConfig(string config): void |
| `metadata` | `?array<string,string>` | Optional | A map of arbitrary key-value pairs for labeling or organizing the agent configuration | getMetadata(): ?array | setMetadata(?array metadata): void |
| `apiVersion` | `?int` | Optional | API version. Defaults to 1<br><br>**Default**: `1` | getApiVersion(): ?int | setApiVersion(?int apiVersion): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\CreateAgentConfigurationV1RequestBuilder;
use DeepgramLib\ApiHelper;

$createAgentConfigurationV1Request = CreateAgentConfigurationV1RequestBuilder::init(
    'config2'
)
    ->metadata(
        [
            'key0' => 'metadata3'
        ]
    )
    ->apiVersion(1)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

