
# List Project Invites V1 Response

*This model accepts additional fields of type array.*

## Structure

`ListProjectInvitesV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `invites` | [`?(ListProjectInvitesV1ResponseInvitesItems[])`](../../doc/models/list-project-invites-v1-response-invites-items.md) | Optional | - | getInvites(): ?array | setInvites(?array invites): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use RestApiLib\Models\Builders\ListProjectInvitesV1ResponseBuilder;
use RestApiLib\Models\Builders\ListProjectInvitesV1ResponseInvitesItemsBuilder;
use RestApiLib\ApiHelper;

$listProjectInvitesV1Response = ListProjectInvitesV1ResponseBuilder::init()
    ->invites(
        [
            ListProjectInvitesV1ResponseInvitesItemsBuilder::init()
                ->email('email8')
                ->scope('scope4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

