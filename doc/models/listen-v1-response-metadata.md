
# Listen V1 Response Metadata

*This model accepts additional fields of type array.*

## Structure

`ListenV1ResponseMetadata`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `transactionKey` | `?string` | Optional | **Default**: `'deprecated'` | getTransactionKey(): ?string | setTransactionKey(?string transactionKey): void |
| `requestId` | `string` | Required | - | getRequestId(): string | setRequestId(string requestId): void |
| `sha256` | `string` | Required | - | getSha256(): string | setSha256(string sha256): void |
| `created` | `DateTime` | Required | - | getCreated(): \DateTime | setCreated(\DateTime created): void |
| `duration` | `float` | Required | - | getDuration(): float | setDuration(float duration): void |
| `channels` | `int` | Required | - | getChannels(): int | setChannels(int channels): void |
| `models` | `string[]` | Required | - | getModels(): array | setModels(array models): void |
| `modelInfo` | `array` | Required | - | getModelInfo(): array | setModelInfo(array modelInfo): void |
| `summaryInfo` | [`?ListenV1ResponseMetadataSummaryInfo`](../../doc/models/listen-v1-response-metadata-summary-info.md) | Optional | - | getSummaryInfo(): ?ListenV1ResponseMetadataSummaryInfo | setSummaryInfo(?ListenV1ResponseMetadataSummaryInfo summaryInfo): void |
| `sentimentInfo` | [`?ListenV1ResponseMetadataSentimentInfo`](../../doc/models/listen-v1-response-metadata-sentiment-info.md) | Optional | - | getSentimentInfo(): ?ListenV1ResponseMetadataSentimentInfo | setSentimentInfo(?ListenV1ResponseMetadataSentimentInfo sentimentInfo): void |
| `topicsInfo` | [`?ListenV1ResponseMetadataTopicsInfo`](../../doc/models/listen-v1-response-metadata-topics-info.md) | Optional | - | getTopicsInfo(): ?ListenV1ResponseMetadataTopicsInfo | setTopicsInfo(?ListenV1ResponseMetadataTopicsInfo topicsInfo): void |
| `intentsInfo` | [`?ListenV1ResponseMetadataIntentsInfo`](../../doc/models/listen-v1-response-metadata-intents-info.md) | Optional | - | getIntentsInfo(): ?ListenV1ResponseMetadataIntentsInfo | setIntentsInfo(?ListenV1ResponseMetadataIntentsInfo intentsInfo): void |
| `tags` | `?(string[])` | Optional | - | getTags(): ?array | setTags(?array tags): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListenV1ResponseMetadataBuilder;
use DeepgramLib\Utils\DateTimeHelper;
use DeepgramLib\ApiHelper;
use DeepgramLib\Models\Builders\ListenV1ResponseMetadataSummaryInfoBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseMetadataSentimentInfoBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseMetadataTopicsInfoBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseMetadataIntentsInfoBuilder;

$listenV1ResponseMetadata = ListenV1ResponseMetadataBuilder::init(
    '00000a0c-0000-0000-0000-000000000000',
    'sha2568',
    DateTimeHelper::fromRfc3339DateTimeRequired('2016-03-13T12:52:32.123Z'),
    75.12,
    174,
    [
        'models2'
    ],
    ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
)
    ->transactionKey('deprecated')
    ->summaryInfo(
        ListenV1ResponseMetadataSummaryInfoBuilder::init()
            ->modelUuid('model_uuid4')
            ->inputTokens(120)
            ->outputTokens(120)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->sentimentInfo(
        ListenV1ResponseMetadataSentimentInfoBuilder::init()
            ->modelUuid('model_uuid6')
            ->inputTokens(86)
            ->outputTokens(86)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->topicsInfo(
        ListenV1ResponseMetadataTopicsInfoBuilder::init()
            ->modelUuid('model_uuid8')
            ->inputTokens(156)
            ->outputTokens(156)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->intentsInfo(
        ListenV1ResponseMetadataIntentsInfoBuilder::init()
            ->modelUuid('model_uuid6')
            ->inputTokens(198)
            ->outputTokens(198)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

