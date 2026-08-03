
# Listen V1 Response Results Utterances Items

*This model accepts additional fields of type array.*

## Structure

`ListenV1ResponseResultsUtterancesItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `start` | `?float` | Optional | - | getStart(): ?float | setStart(?float start): void |
| `end` | `?float` | Optional | - | getEnd(): ?float | setEnd(?float end): void |
| `confidence` | `?float` | Optional | - | getConfidence(): ?float | setConfidence(?float confidence): void |
| `channel` | `?int` | Optional | - | getChannel(): ?int | setChannel(?int channel): void |
| `transcript` | `?string` | Optional | - | getTranscript(): ?string | setTranscript(?string transcript): void |
| `words` | [`?(ListenV1ResponseResultsUtterancesItemsWordsItems[])`](../../doc/models/listen-v1-response-results-utterances-items-words-items.md) | Optional | - | getWords(): ?array | setWords(?array words): void |
| `speaker` | `?int` | Optional | - | getSpeaker(): ?int | setSpeaker(?int speaker): void |
| `id` | `?string` | Optional | - | getId(): ?string | setId(?string id): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListenV1ResponseResultsUtterancesItemsBuilder;
use RestApiLib\ApiHelper;

$listenV1ResponseResultsUtterancesItems = ListenV1ResponseResultsUtterancesItemsBuilder::init()
    ->start(55.44)
    ->end(99.38)
    ->confidence(53.54)
    ->channel(164)
    ->transcript('transcript8')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

