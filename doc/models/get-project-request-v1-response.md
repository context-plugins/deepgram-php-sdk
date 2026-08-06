
# Get Project Request V1 Response

*This model accepts additional fields of type array.*

## Structure

`GetProjectRequestV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `request` | [`?ProjectRequestResponse`](../../doc/models/project-request-response.md) | Optional | A single request | getRequest(): ?ProjectRequestResponse | setRequest(?ProjectRequestResponse request): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\GetProjectRequestV1ResponseBuilder;
use DeepgramLib\Models\Builders\ProjectRequestResponseBuilder;
use DeepgramLib\Utils\DateTimeHelper;
use DeepgramLib\ApiHelper;

$getProjectRequestV1Response = GetProjectRequestV1ResponseBuilder::init()
    ->request(
        ProjectRequestResponseBuilder::init()
            ->requestId('request_id2')
            ->projectUuid('project_uuid6')
            ->created(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->path('path0')
            ->apiKeyId('api_key_id0')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

