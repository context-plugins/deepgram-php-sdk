
# List Project Requests V1 Response

*This model accepts additional fields of type array.*

## Structure

`ListProjectRequestsV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `page` | `?float` | Optional | The page number of the paginated response | getPage(): ?float | setPage(?float page): void |
| `limit` | `?float` | Optional | The number of results per page | getLimit(): ?float | setLimit(?float limit): void |
| `requests` | [`?(ProjectRequestResponse[])`](../../doc/models/project-request-response.md) | Optional | - | getRequests(): ?array | setRequests(?array requests): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListProjectRequestsV1ResponseBuilder;
use DeepgramLib\Models\Builders\ProjectRequestResponseBuilder;
use DeepgramLib\Utils\DateTimeHelper;
use DeepgramLib\ApiHelper;

$listProjectRequestsV1Response = ListProjectRequestsV1ResponseBuilder::init()
    ->page(239.24)
    ->limit(110.1)
    ->requests(
        [
            ProjectRequestResponseBuilder::init()
                ->requestId('request_id0')
                ->projectUuid('project_uuid8')
                ->created(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->path('path2')
                ->apiKeyId('api_key_id2')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ProjectRequestResponseBuilder::init()
                ->requestId('request_id0')
                ->projectUuid('project_uuid8')
                ->created(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->path('path2')
                ->apiKeyId('api_key_id2')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ProjectRequestResponseBuilder::init()
                ->requestId('request_id0')
                ->projectUuid('project_uuid8')
                ->created(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->path('path2')
                ->apiKeyId('api_key_id2')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

