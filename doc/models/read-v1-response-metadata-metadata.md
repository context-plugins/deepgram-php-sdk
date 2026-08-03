
# Read V1 Response Metadata Metadata

*This model accepts additional fields of type array.*

## Structure

`ReadV1ResponseMetadataMetadata`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `requestId` | `?string` | Optional | - | getRequestId(): ?string | setRequestId(?string requestId): void |
| `created` | `?DateTime` | Optional | - | getCreated(): ?\DateTime | setCreated(?\DateTime created): void |
| `language` | `?string` | Optional | - | getLanguage(): ?string | setLanguage(?string language): void |
| `summaryInfo` | [`?ReadV1ResponseMetadataMetadataSummaryInfo`](../../doc/models/read-v1-response-metadata-metadata-summary-info.md) | Optional | - | getSummaryInfo(): ?ReadV1ResponseMetadataMetadataSummaryInfo | setSummaryInfo(?ReadV1ResponseMetadataMetadataSummaryInfo summaryInfo): void |
| `sentimentInfo` | [`?ReadV1ResponseMetadataMetadataSentimentInfo`](../../doc/models/read-v1-response-metadata-metadata-sentiment-info.md) | Optional | - | getSentimentInfo(): ?ReadV1ResponseMetadataMetadataSentimentInfo | setSentimentInfo(?ReadV1ResponseMetadataMetadataSentimentInfo sentimentInfo): void |
| `topicsInfo` | [`?ReadV1ResponseMetadataMetadataTopicsInfo`](../../doc/models/read-v1-response-metadata-metadata-topics-info.md) | Optional | - | getTopicsInfo(): ?ReadV1ResponseMetadataMetadataTopicsInfo | setTopicsInfo(?ReadV1ResponseMetadataMetadataTopicsInfo topicsInfo): void |
| `intentsInfo` | [`?ReadV1ResponseMetadataMetadataIntentsInfo`](../../doc/models/read-v1-response-metadata-metadata-intents-info.md) | Optional | - | getIntentsInfo(): ?ReadV1ResponseMetadataMetadataIntentsInfo | setIntentsInfo(?ReadV1ResponseMetadataMetadataIntentsInfo intentsInfo): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ReadV1ResponseMetadataMetadataBuilder;
use RestApiLib\Utils\DateTimeHelper;
use RestApiLib\Models\Builders\ReadV1ResponseMetadataMetadataSummaryInfoBuilder;
use RestApiLib\ApiHelper;
use RestApiLib\Models\Builders\ReadV1ResponseMetadataMetadataSentimentInfoBuilder;

$readV1ResponseMetadataMetadata = ReadV1ResponseMetadataMetadataBuilder::init()
    ->requestId('000016b8-0000-0000-0000-000000000000')
    ->created(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->language('language4')
    ->summaryInfo(
        ReadV1ResponseMetadataMetadataSummaryInfoBuilder::init()
            ->modelUuid('00000e32-0000-0000-0000-000000000000')
            ->inputTokens(120)
            ->outputTokens(120)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->sentimentInfo(
        ReadV1ResponseMetadataMetadataSentimentInfoBuilder::init()
            ->modelUuid('00001640-0000-0000-0000-000000000000')
            ->inputTokens(86)
            ->outputTokens(86)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

