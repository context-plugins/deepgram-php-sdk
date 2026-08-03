
# List Project Purchases V1 Response Orders Items

*This model accepts additional fields of type array.*

## Structure

`ListProjectPurchasesV1ResponseOrdersItems`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `orderId` | `?string` | Optional | - | getOrderId(): ?string | setOrderId(?string orderId): void |
| `expiration` | `?DateTime` | Optional | - | getExpiration(): ?\DateTime | setExpiration(?\DateTime expiration): void |
| `created` | `?DateTime` | Optional | - | getCreated(): ?\DateTime | setCreated(?\DateTime created): void |
| `amount` | `?float` | Optional | - | getAmount(): ?float | setAmount(?float amount): void |
| `units` | `?string` | Optional | - | getUnits(): ?string | setUnits(?string units): void |
| `orderType` | `?string` | Optional | - | getOrderType(): ?string | setOrderType(?string orderType): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListProjectPurchasesV1ResponseOrdersItemsBuilder;
use RestApiLib\Utils\DateTimeHelper;
use RestApiLib\ApiHelper;

$listProjectPurchasesV1ResponseOrdersItems = ListProjectPurchasesV1ResponseOrdersItemsBuilder::init()
    ->orderId('00000276-0000-0000-0000-000000000000')
    ->expiration(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->created(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->amount(103.78)
    ->units('units8')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

