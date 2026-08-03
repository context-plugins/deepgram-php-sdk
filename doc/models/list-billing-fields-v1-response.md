
# List Billing Fields V1 Response

*This model accepts additional fields of type array.*

## Structure

`ListBillingFieldsV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accessors` | `?(string[])` | Optional | List of accessor UUIDs for the time period | getAccessors(): ?array | setAccessors(?array accessors): void |
| `deployments` | [`?(string(ListBillingFieldsV1ResponseDeploymentsItems)[])`](../../doc/models/list-billing-fields-v1-response-deployments-items.md) | Optional | List of deployment types for the time period | getDeployments(): ?array | setDeployments(?array deployments): void |
| `tags` | `?(string[])` | Optional | List of tags for the time period | getTags(): ?array | setTags(?array tags): void |
| `lineItems` | `?array<string,string>` | Optional | Map of line item names to human-readable descriptions for the time period | getLineItems(): ?array | setLineItems(?array lineItems): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListBillingFieldsV1ResponseBuilder;
use RestApiLib\Models\ListBillingFieldsV1ResponseDeploymentsItems;
use RestApiLib\ApiHelper;

$listBillingFieldsV1Response = ListBillingFieldsV1ResponseBuilder::init()
    ->accessors(
        [
            '000000de-0000-0000-0000-000000000000',
            '000000dd-0000-0000-0000-000000000000',
            '000000dc-0000-0000-0000-000000000000'
        ]
    )
    ->deployments(
        [
            ListBillingFieldsV1ResponseDeploymentsItems::BETA,
            ListBillingFieldsV1ResponseDeploymentsItems::SELFHOSTED,
            ListBillingFieldsV1ResponseDeploymentsItems::DEDICATED
        ]
    )
    ->tags(
        [
            'tags5'
        ]
    )
    ->lineItems(
        [
            'key0' => 'line_items1'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

