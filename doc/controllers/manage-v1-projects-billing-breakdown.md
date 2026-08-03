# Manage V1 Projects Billing Breakdown

```php
$manageV1ProjectsBillingBreakdownApi = $client->getManageV1ProjectsBillingBreakdownApi();
```

## Class Name

`ManageV1ProjectsBillingBreakdownApi`


# List

Retrieves the billing summary for a specific project, with various filter options or by grouping options.

:information_source: **Note** This endpoint does not require authentication.

```php
function mList(
    string $projectId,
    string $authorization,
    ?\DateTime $start = null,
    ?\DateTime $end = null,
    ?string $accessor = null,
    ?string $deployment = null,
    ?string $tag = null,
    ?string $lineItem = null,
    ?array $grouping = null
): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectId` | `string` | Template, Required | The unique identifier of the project |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |
| `start` | `?DateTime` | Query, Optional | Start date of the requested date range. Format accepted is YYYY-MM-DD |
| `end` | `?DateTime` | Query, Optional | End date of the requested date range. Format accepted is YYYY-MM-DD |
| `accessor` | `?string` | Query, Optional | Filter for requests where a specific accessor was used |
| `deployment` | [`?string(V1ProjectsProjectIdBillingBreakdownGetParametersDeployment)`](../../doc/models/v1-projects-project-id-billing-breakdown-get-parameters-deployment.md) | Query, Optional | Filter for requests where a specific deployment was used |
| `tag` | `?string` | Query, Optional | Filter for requests where a specific tag was used |
| `lineItem` | `?string` | Query, Optional | Filter requests by line item (e.g. streaming::nova-3) |
| `grouping` | [`?(string(V1ProjectsProjectIdBillingBreakdownGetParametersGroupingSchemaItems)[])`](../../doc/models/v1-projects-project-id-billing-breakdown-get-parameters-grouping-schema-items.md) | Query, Optional | Group billing breakdown by one or more dimensions (accessor, deployment, line_item, tags) |

## Response Type

**200**: Billing breakdown response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`BillingBreakdownV1Response`](../../doc/models/billing-breakdown-v1-response.md).

## Example Usage

```php
$projectId = 'project_id6';

$authorization = 'Authorization8';

$manageV1ProjectsBillingBreakdownApi = $client->getManageV1ProjectsBillingBreakdownApi();
$apiResponse = $manageV1ProjectsBillingBreakdownApi->mList(
    $projectId,
    $authorization
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'BillingBreakdownV1Response:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid Request | `ApiException` |

