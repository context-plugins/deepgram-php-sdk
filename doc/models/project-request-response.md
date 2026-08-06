
# Project Request Response

A single request

*This model accepts additional fields of type array.*

## Structure

`ProjectRequestResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `requestId` | `?string` | Optional | The unique identifier of the request | getRequestId(): ?string | setRequestId(?string requestId): void |
| `projectUuid` | `?string` | Optional | The unique identifier of the project | getProjectUuid(): ?string | setProjectUuid(?string projectUuid): void |
| `created` | `?DateTime` | Optional | The date and time the request was created | getCreated(): ?\DateTime | setCreated(?\DateTime created): void |
| `path` | `?string` | Optional | The API path of the request | getPath(): ?string | setPath(?string path): void |
| `apiKeyId` | `?string` | Optional | The unique identifier of the API key | getApiKeyId(): ?string | setApiKeyId(?string apiKeyId): void |
| `response` | `?array` | Optional | The response of the request | getResponse(): ?array | setResponse(?array response): void |
| `code` | `?float` | Optional | The response code of the request | getCode(): ?float | setCode(?float code): void |
| `deployment` | `?string` | Optional | The deployment type | getDeployment(): ?string | setDeployment(?string deployment): void |
| `callback` | `?string` | Optional | The callback URL for the request | getCallback(): ?string | setCallback(?string callback): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ProjectRequestResponseBuilder;
use DeepgramLib\Utils\DateTimeHelper;
use DeepgramLib\ApiHelper;

$projectRequestResponse = ProjectRequestResponseBuilder::init()
    ->requestId('request_id6')
    ->projectUuid('project_uuid2')
    ->created(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->path('path6')
    ->apiKeyId('api_key_id6')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

