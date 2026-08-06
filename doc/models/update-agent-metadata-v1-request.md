
# Update Agent Metadata V1 Request

Request body for updating agent configuration metadata

*This model accepts additional fields of type array.*

## Structure

`UpdateAgentMetadataV1Request`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `metadata` | `array<string,string>` | Required | A map of string key-value pairs to associate with this agent configuration | getMetadata(): array | setMetadata(array metadata): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\UpdateAgentMetadataV1RequestBuilder;
use DeepgramLib\ApiHelper;

$updateAgentMetadataV1Request = UpdateAgentMetadataV1RequestBuilder::init(
    [
        'key0' => 'metadata7',
        'key1' => 'metadata8',
        'key2' => 'metadata9'
    ]
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

