
# Listen V1 Response Error Exception

The standard transcription response

*This model accepts additional fields of type array.*

## Structure

`ListenV1ResponseErrorException`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `metadata` | [`ListenV1ResponseMetadata`](../../doc/models/listen-v1-response-metadata.md) | Required | - | getMetadata(): ListenV1ResponseMetadata | setMetadata(ListenV1ResponseMetadata metadata): void |
| `results` | [`ListenV1ResponseResults`](../../doc/models/listen-v1-response-results.md) | Required | - | getResults(): ListenV1ResponseResults | setResults(ListenV1ResponseResults results): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

