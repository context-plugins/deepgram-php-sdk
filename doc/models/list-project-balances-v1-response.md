
# List Project Balances V1 Response

*This model accepts additional fields of type array.*

## Structure

`ListProjectBalancesV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `balances` | [`?(ListProjectBalancesV1ResponseBalancesItems[])`](../../doc/models/list-project-balances-v1-response-balances-items.md) | Optional | - | getBalances(): ?array | setBalances(?array balances): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListProjectBalancesV1ResponseBuilder;
use RestApiLib\Models\Builders\ListProjectBalancesV1ResponseBalancesItemsBuilder;
use RestApiLib\ApiHelper;

$listProjectBalancesV1Response = ListProjectBalancesV1ResponseBuilder::init()
    ->balances(
        [
            ListProjectBalancesV1ResponseBalancesItemsBuilder::init()
                ->balanceId('balance_id2')
                ->amount(149.62)
                ->units('units4')
                ->purchaseOrderId('purchase_order_id0')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ListProjectBalancesV1ResponseBalancesItemsBuilder::init()
                ->balanceId('balance_id2')
                ->amount(149.62)
                ->units('units4')
                ->purchaseOrderId('purchase_order_id0')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ListProjectBalancesV1ResponseBalancesItemsBuilder::init()
                ->balanceId('balance_id2')
                ->amount(149.62)
                ->units('units4')
                ->purchaseOrderId('purchase_order_id0')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

