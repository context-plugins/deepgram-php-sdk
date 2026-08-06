
# Custom Header Signature



Documentation for accessing and setting credentials for ApiKeyAuth.

## Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| Authorization | `string` | Use `Authorization: Token <API_KEY>`<br>Example: `Authorization: Token 12345abcdef` | `authorization` | `getAuthorization()` |



**Note:** Auth credentials can be set using `ApiKeyAuthCredentialsBuilder::init()` in `apiKeyAuthCredentials` method in the client builder and accessed through `getApiKeyAuthCredentials` method in the client instance.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```php
use DeepgramLib\Authentication\ApiKeyAuthCredentialsBuilder;
use DeepgramLib\DeepgramClientBuilder;

$client = DeepgramClientBuilder::init()
    ->apiKeyAuthCredentials(
        ApiKeyAuthCredentialsBuilder::init(
            'Authorization'
        )
    )
    ->build();
```


