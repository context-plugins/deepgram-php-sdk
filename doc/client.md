
# Client Class Documentation

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](../README.md#environments) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| timeout | `int` | Timeout for API calls in seconds.<br>*Default*: `30` |
| enableRetries | `bool` | Whether to enable retries and backoff feature.<br>*Default*: `false` |
| numberOfRetries | `int` | The number of retries to make.<br>*Default*: `0` |
| retryInterval | `float` | The retry time interval between the endpoint calls.<br>*Default*: `1` |
| backOffFactor | `float` | Exponential backoff factor to increase interval between retries.<br>*Default*: `2` |
| maximumRetryWaitTime | `int` | The maximum wait time in seconds for overall retrying requests.<br>*Default*: `0` |
| retryOnTimeout | `bool` | Whether to retry on request timeout.<br>*Default*: `true` |
| httpStatusCodesToRetry | `array` | Http status codes to retry against.<br>*Default*: `408, 413, 429, 500, 502, 503, 504, 521, 522, 524, 408, 413, 429, 500, 502, 503, 504, 521, 522, 524` |
| httpMethodsToRetry | `array` | Http methods to retry against.<br>*Default*: `'GET', 'PUT', 'GET', 'PUT'` |
| loggingConfiguration | [`LoggingConfigurationBuilder`](../doc/logging-configuration-builder.md) | Represents the logging configurations for API calls |
| proxyConfiguration | [`ProxyConfigurationBuilder`](../doc/proxy-configuration-builder.md) | Represents the proxy configurations for API calls |
| apiKeyAuthCredentials | [`ApiKeyAuthCredentials`](auth/custom-header-signature.md) | The Credentials Setter for Custom Header Signature |
| jwtAuthCredentials | [`JwtAuthCredentials`](auth/oauth-2-bearer-token.md) | The Credentials Setter for OAuth 2 Bearer token |

The API client can be initialized as follows:

```php
use RestApiLib\Logging\LoggingConfigurationBuilder;
use RestApiLib\Logging\RequestLoggingConfigurationBuilder;
use RestApiLib\Logging\ResponseLoggingConfigurationBuilder;
use Psr\Log\LogLevel;
use RestApiLib\Environment;
use RestApiLib\Authentication\ApiKeyAuthCredentialsBuilder;
use RestApiLib\Authentication\JwtAuthCredentialsBuilder;
use RestApiLib\RestApiClientBuilder;

$client = RestApiClientBuilder::init()
    ->apiKeyAuthCredentials(
        ApiKeyAuthCredentialsBuilder::init(
            'Authorization'
        )
    )
    ->jwtAuthCredentials(
        JwtAuthCredentialsBuilder::init(
            'AccessToken'
        )
    )
    ->environment(Environment::PRODUCTION)
    ->loggingConfiguration(
        LoggingConfigurationBuilder::init()
            ->level(LogLevel::INFO)
            ->requestConfiguration(RequestLoggingConfigurationBuilder::init()->body(true))
            ->responseConfiguration(ResponseLoggingConfigurationBuilder::init()->headers(true))
    )
    ->build();
```

## REST API Client

The gateway for the SDK. This class acts as a factory for the Apis and also holds the configuration of the SDK.

## Apis

| Name | Description |
|  --- | --- |
| getAgentV1SettingsThinkModelsApi() | Gets AgentV1SettingsThinkModelsApi |
| getVoiceAgentConfigurationsApi() | Gets VoiceAgentConfigurationsApi |
| getVoiceAgentVariablesApi() | Gets VoiceAgentVariablesApi |
| getListenV1MediaApi() | Gets ListenV1MediaApi |
| getSpeakV1AudioApi() | Gets SpeakV1AudioApi |
| getReadV1TextApi() | Gets ReadV1TextApi |
| getManageV1ProjectsApi() | Gets ManageV1ProjectsApi |
| getManageV1ProjectsModelsApi() | Gets ManageV1ProjectsModelsApi |
| getManageV1ModelsApi() | Gets ManageV1ModelsApi |
| getManageV1ProjectsKeysApi() | Gets ManageV1ProjectsKeysApi |
| getManageV1ProjectsMembersApi() | Gets ManageV1ProjectsMembersApi |
| getManageV1ProjectsMembersScopesApi() | Gets ManageV1ProjectsMembersScopesApi |
| getManageV1ProjectsMembersInvitesApi() | Gets ManageV1ProjectsMembersInvitesApi |
| getManageV1ProjectsRequestsApi() | Gets ManageV1ProjectsRequestsApi |
| getManageV1ProjectsUsageApi() | Gets ManageV1ProjectsUsageApi |
| getManageV1ProjectsUsageFieldsApi() | Gets ManageV1ProjectsUsageFieldsApi |
| getManageV1ProjectsUsageBreakdownApi() | Gets ManageV1ProjectsUsageBreakdownApi |
| getManageV1ProjectsBillingBalancesApi() | Gets ManageV1ProjectsBillingBalancesApi |
| getManageV1ProjectsBillingBreakdownApi() | Gets ManageV1ProjectsBillingBreakdownApi |
| getManageV1ProjectsBillingFieldsApi() | Gets ManageV1ProjectsBillingFieldsApi |
| getManageV1ProjectsBillingPurchasesApi() | Gets ManageV1ProjectsBillingPurchasesApi |
| getSelfHostedV1DistributionCredentialsApi() | Gets SelfHostedV1DistributionCredentialsApi |
| getAuthV1TokensApi() | Gets AuthV1TokensApi |
| getSpeakV2AudioApi() | Gets SpeakV2AudioApi |

