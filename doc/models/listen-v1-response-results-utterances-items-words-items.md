
# Listen V1 Response Results Utterances Items Words Items

*This model accepts additional fields of type array.*

## Structure

`ListenV1ResponseResultsUtterancesItemsWordsItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `word` | `?string` | Optional | - | getWord(): ?string | setWord(?string word): void |
| `start` | `?float` | Optional | - | getStart(): ?float | setStart(?float start): void |
| `end` | `?float` | Optional | - | getEnd(): ?float | setEnd(?float end): void |
| `confidence` | `?float` | Optional | - | getConfidence(): ?float | setConfidence(?float confidence): void |
| `speaker` | `?int` | Optional | - | getSpeaker(): ?int | setSpeaker(?int speaker): void |
| `speakerConfidence` | `?float` | Optional | - | getSpeakerConfidence(): ?float | setSpeakerConfidence(?float speakerConfidence): void |
| `punctuatedWord` | `?string` | Optional | - | getPunctuatedWord(): ?string | setPunctuatedWord(?string punctuatedWord): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListenV1ResponseResultsUtterancesItemsWordsItemsBuilder;
use DeepgramLib\ApiHelper;

$listenV1ResponseResultsUtterancesItemsWordsItems = ListenV1ResponseResultsUtterancesItemsWordsItemsBuilder::init()
    ->word('word6')
    ->start(61.58)
    ->end(105.52)
    ->confidence(59.68)
    ->speaker(26)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

