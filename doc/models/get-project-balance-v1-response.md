
# Get Project Balance V1 Response

*This model accepts additional fields of type array.*

## Structure

`GetProjectBalanceV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `balanceId` | `?string` | Optional | The unique identifier of the balance | getBalanceId(): ?string | setBalanceId(?string balanceId): void |
| `amount` | `?float` | Optional | The amount of the balance<br><br>**Default**: `0` | getAmount(): ?float | setAmount(?float amount): void |
| `units` | `?string` | Optional | The units of the balance, such as "USD" | getUnits(): ?string | setUnits(?string units): void |
| `purchaseOrderId` | `?string` | Optional | Description or reference of the purchase | getPurchaseOrderId(): ?string | setPurchaseOrderId(?string purchaseOrderId): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\GetProjectBalanceV1ResponseBuilder;
use DeepgramLib\ApiHelper;

$getProjectBalanceV1Response = GetProjectBalanceV1ResponseBuilder::init()
    ->balanceId('balance_id6')
    ->amount(0)
    ->units('units8')
    ->purchaseOrderId('purchase_order_id4')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

