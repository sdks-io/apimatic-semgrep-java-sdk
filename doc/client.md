
# Client Class Documentation

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](../README.md#environments) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| httpClientConfig | [`Consumer<HttpClientConfiguration.Builder>`](../doc/http-client-configuration-builder.md) | Set up Http Client Configuration instance. |
| loggingConfig | [`Consumer<ApiLoggingConfiguration.Builder>`](../doc/api-logging-configuration-builder.md) | Set up Logging Configuration instance. |
| semgrepAdminJwtCredentials | [`SemgrepAdminJwtCredentials`](auth/oauth-2-bearer-token.md) | The Credentials Setter for OAuth 2 Bearer token |
| semgrepJwtCredentials | [`SemgrepJwtCredentials`](auth/oauth-2-bearer-token-1.md) | The Credentials Setter for OAuth 2 Bearer token |
| semgrepWebTokenCredentials | [`SemgrepWebTokenCredentials`](auth/oauth-2-bearer-token-2.md) | The Credentials Setter for OAuth 2 Bearer token |

The API client can be initialized as follows:

```java
import dev.semgrep.Environment;
import dev.semgrep.SemgrepWebAppClient;
import dev.semgrep.authentication.SemgrepAdminJwtModel;
import dev.semgrep.authentication.SemgrepJwtModel;
import dev.semgrep.authentication.SemgrepWebTokenModel;
import dev.semgrep.exceptions.ApiException;
import dev.semgrep.http.response.ApiResponse;
import org.slf4j.event.Level;

public class Program {
    public static void main(String[] args) {
        SemgrepWebAppClient client = new SemgrepWebAppClient.Builder()
            .loggingConfig(builder -> builder
                    .level(Level.DEBUG)
                    .requestConfig(logConfigBuilder -> logConfigBuilder.body(true))
                    .responseConfig(logConfigBuilder -> logConfigBuilder.headers(true)))
            .httpClientConfig(configBuilder -> configBuilder
                    .timeout(0))
            .semgrepAdminJwtCredentials(new SemgrepAdminJwtModel.Builder(
                    "AccessToken"
                )
                .build())
            .semgrepJwtCredentials(new SemgrepJwtModel.Builder(
                    "AccessToken"
                )
                .build())
            .semgrepWebTokenCredentials(new SemgrepWebTokenModel.Builder(
                    "AccessToken"
                )
                .build())
            .environment(Environment.PRODUCTION)
            .build();

    }
}
```

## Semgrep Web AppClient Class

The gateway for the SDK. This class acts as a factory for the Apis and also holds the configuration of the SDK.

### Apis

| Name | Description | Return Type |
|  --- | --- | --- |
| `getDeploymentsServiceApi()` | Provides access to DeploymentsService controller. | `DeploymentsServiceApi` |
| `getFindingsServiceApi()` | Provides access to FindingsService controller. | `FindingsServiceApi` |
| `getMiscServiceApi()` | Provides access to MiscService controller. | `MiscServiceApi` |
| `getPoliciesServiceApi()` | Provides access to PoliciesService controller. | `PoliciesServiceApi` |
| `getProjectsServiceApi()` | Provides access to ProjectsService controller. | `ProjectsServiceApi` |
| `getScansServiceApi()` | Provides access to ScansService controller. | `ScansServiceApi` |
| `getSecretsServiceApi()` | Provides access to SecretsService controller. | `SecretsServiceApi` |
| `getSupplyChainServiceApi()` | Provides access to SupplyChainService controller. | `SupplyChainServiceApi` |
| `getTicketingServiceApi()` | Provides access to TicketingService controller. | `TicketingServiceApi` |
| `getTriageServiceApi()` | Provides access to TriageService controller. | `TriageServiceApi` |

### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `shutdown()` | Shutdown the underlying HttpClient instance. | `void` |
| `getEnvironment()` | Current API environment. | `Environment` |
| `getHttpClient()` | The HTTP Client instance to use for making HTTP requests. | `HttpClient` |
| `getHttpClientConfig()` | Http Client Configuration instance. | [`ReadonlyHttpClientConfiguration`](../doc/http-client-configuration.md) |
| `getLoggingConfig()` | Logging Configuration instance. | [`ReadonlyLoggingConfiguration`](../doc/api-logging-configuration.md) |
| `getSemgrepAdminJwtCredentials()` | The credentials to use with SemgrepAdminJwt. | [`SemgrepAdminJwtCredentials`](auth/oauth-2-bearer-token.md) |
| `getSemgrepJwtCredentials()` | The credentials to use with SemgrepJwt. | [`SemgrepJwtCredentials`](auth/oauth-2-bearer-token-1.md) |
| `getSemgrepWebTokenCredentials()` | The credentials to use with SemgrepWebToken. | [`SemgrepWebTokenCredentials`](auth/oauth-2-bearer-token-2.md) |
| `getBaseUri(Server server)` | Get base URI by current environment | `String` |
| `getBaseUri()` | Get base URI by current environment | `String` |

