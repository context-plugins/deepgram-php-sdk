# Auth V1 Tokens

```php
$authV1TokensApi = $client->getAuthV1TokensApi();
```

## Class Name

`AuthV1TokensApi`


# Grant

Generates a temporary JSON Web Token (JWT) with a 30-second (by default) TTL and usage::write permission for core voice APIs, requiring an API key with Member or higher authorization. Tokens created with this endpoint will not work with the Manage APIs.

:information_source: **Note** This endpoint does not require authentication.

```php
function grant(string $authorization, ?GrantV1Request $body = null): ApiResponse
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authorization` | `string` | Header, Required | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` |
| `body` | [`?GrantV1Request`](../../doc/models/grant-v1-request.md) | Body, Optional | Time to live settings |

## Response Type

**200**: Grant response

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` method on this instance returns the response data which is of type [`GrantV1Response`](../../doc/models/grant-v1-response.md).

## Example Usage

```php
$authorization = 'Authorization8';

$authV1TokensApi = $client->getAuthV1TokensApi();
$apiResponse = $authV1TokensApi->grant($authorization);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'GrantV1Response:';
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

