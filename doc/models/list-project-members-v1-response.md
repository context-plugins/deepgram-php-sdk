
# List Project Members V1 Response

*This model accepts additional fields of type array.*

## Structure

`ListProjectMembersV1Response`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `members` | [`?(ListProjectMembersV1ResponseMembersItems[])`](../../doc/models/list-project-members-v1-response-members-items.md) | Optional | - | getMembers(): ?array | setMembers(?array members): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |

## Example

```php
use DeepgramLib\Models\Builders\ListProjectMembersV1ResponseBuilder;
use DeepgramLib\Models\Builders\ListProjectMembersV1ResponseMembersItemsBuilder;
use DeepgramLib\ApiHelper;

$listProjectMembersV1Response = ListProjectMembersV1ResponseBuilder::init()
    ->members(
        [
            ListProjectMembersV1ResponseMembersItemsBuilder::init()
                ->memberId('member_id2')
                ->scopes(
                    [
                        'scopes4',
                        'scopes5',
                        'scopes6'
                    ]
                )
                ->email('email8')
                ->firstName('first_name8')
                ->lastName('last_name6')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ListProjectMembersV1ResponseMembersItemsBuilder::init()
                ->memberId('member_id2')
                ->scopes(
                    [
                        'scopes4',
                        'scopes5',
                        'scopes6'
                    ]
                )
                ->email('email8')
                ->firstName('first_name8')
                ->lastName('last_name6')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```

