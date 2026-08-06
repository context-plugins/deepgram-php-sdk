
# OAuth 2 Bearer token



Documentation for accessing and setting credentials for JwtAuth.

## Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| AccessToken | `string` | The OAuth 2.0 Access Token to use for API requests. | `accessToken` | `getAccessToken()` |



**Note:** Auth credentials can be set using `JwtAuthCredentialsBuilder::init()` in `jwtAuthCredentials` method in the client builder and accessed through `getJwtAuthCredentials` method in the client instance.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```php
use DeepgramLib\Authentication\JwtAuthCredentialsBuilder;
use DeepgramLib\DeepgramClientBuilder;

$client = DeepgramClientBuilder::init()
    ->jwtAuthCredentials(
        JwtAuthCredentialsBuilder::init(
            'AccessToken'
        )
    )
    ->build();
```


