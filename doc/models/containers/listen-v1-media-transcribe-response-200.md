
# Listen V1 Media Transcribe Response 200

## Data Type

`ListenV1Response|ListenV1AcceptedResponse`

## Cases

| Type |
|  --- |
| [`ListenV1Response`](../../../doc/models/listen-v1-response.md) |
| [`ListenV1AcceptedResponse`](../../../doc/models/listen-v1-accepted-response.md) |

## ListenV1Response

### Initialization Code

#### Example

```php
$value = ListenV1ResponseBuilder::init(
    ListenV1ResponseMetadataBuilder::init(
        '000018ae-0000-0000-0000-000000000000',
        'sha2568',
        DateTimeHelper::fromRfc3339DateTimeRequired('2016-03-13T12:52:32.123Z'),
        108.02,
        44,
        [
            'models2'
        ],
        ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
    )
        ->transactionKey('deprecated')
        ->build(),
    ListenV1ResponseResultsBuilder::init(
        [
            ListenV1ResponseResultsChannelsItemsBuilder::init()->build()
        ]
    )->build()
)->build();
```

## ListenV1AcceptedResponse

### Initialization Code

#### Example

```php
$value = ListenV1AcceptedResponseBuilder::init(
    '00000e36-0000-0000-0000-000000000000'
)->build();
```

