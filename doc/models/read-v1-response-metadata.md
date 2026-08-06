
# Read V1 Response Metadata

*This model accepts additional fields of type array.*

## Structure

`ReadV1ResponseMetadata`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `metadata` | [`?ReadV1ResponseMetadataMetadata`](../../doc/models/read-v1-response-metadata-metadata.md) | Optional | - | getMetadata(): ?ReadV1ResponseMetadataMetadata | setMetadata(?ReadV1ResponseMetadataMetadata metadata): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ReadV1ResponseMetadataBuilder;
use DeepgramLib\Models\Builders\ReadV1ResponseMetadataMetadataBuilder;
use DeepgramLib\Utils\DateTimeHelper;
use DeepgramLib\Models\Builders\ReadV1ResponseMetadataMetadataSummaryInfoBuilder;
use DeepgramLib\ApiHelper;
use DeepgramLib\Models\Builders\ReadV1ResponseMetadataMetadataSentimentInfoBuilder;

$readV1ResponseMetadata = ReadV1ResponseMetadataBuilder::init()
    ->metadata(
        ReadV1ResponseMetadataMetadataBuilder::init()
            ->requestId('000018ae-0000-0000-0000-000000000000')
            ->created(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->language('language8')
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
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

