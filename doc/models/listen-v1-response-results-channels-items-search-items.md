
# Listen V1 Response Results Channels Items Search Items

*This model accepts additional fields of type array.*

## Structure

`ListenV1ResponseResultsChannelsItemsSearchItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `query` | `?string` | Optional | - | getQuery(): ?string | setQuery(?string query): void |
| `hits` | [`?(ListenV1ResponseResultsChannelsItemsSearchItemsHitsItems[])`](../../doc/models/listen-v1-response-results-channels-items-search-items-hits-items.md) | Optional | - | getHits(): ?array | setHits(?array hits): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsSearchItemsBuilder;
use DeepgramLib\Models\Builders\ListenV1ResponseResultsChannelsItemsSearchItemsHitsItemsBuilder;
use DeepgramLib\ApiHelper;

$listenV1ResponseResultsChannelsItemsSearchItems = ListenV1ResponseResultsChannelsItemsSearchItemsBuilder::init()
    ->query('query2')
    ->hits(
        [
            ListenV1ResponseResultsChannelsItemsSearchItemsHitsItemsBuilder::init()
                ->confidence(144.74)
                ->start(146.64)
                ->end(190.58)
                ->snippet('snippet0')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ListenV1ResponseResultsChannelsItemsSearchItemsHitsItemsBuilder::init()
                ->confidence(144.74)
                ->start(146.64)
                ->end(190.58)
                ->snippet('snippet0')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

