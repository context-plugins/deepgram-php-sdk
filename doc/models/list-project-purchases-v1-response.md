
# List Project Purchases V1 Response

*This model accepts additional fields of type array.*

## Structure

`ListProjectPurchasesV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `orders` | [`?(ListProjectPurchasesV1ResponseOrdersItems[])`](../../doc/models/list-project-purchases-v1-response-orders-items.md) | Optional | - | getOrders(): ?array | setOrders(?array orders): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListProjectPurchasesV1ResponseBuilder;
use RestApiLib\Models\Builders\ListProjectPurchasesV1ResponseOrdersItemsBuilder;
use RestApiLib\Utils\DateTimeHelper;
use RestApiLib\ApiHelper;

$listProjectPurchasesV1Response = ListProjectPurchasesV1ResponseBuilder::init()
    ->orders(
        [
            ListProjectPurchasesV1ResponseOrdersItemsBuilder::init()
                ->orderId('00000d9e-0000-0000-0000-000000000000')
                ->expiration(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->created(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->amount(244.94)
                ->units('units2')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

