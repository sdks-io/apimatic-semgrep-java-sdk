
# Getting Started with Semgrep Web App

## Introduction

Welcome to Semgrep's portal for the Semgrep AppSec Platform web API.

### Introduction

Semgrep is a fast, open-source, static analysis tool for finding bugs and enforcing code standards at editor,
commit, and CI time. [Get started.](https://semgrep.dev/docs/getting-started/)

This API is documented in the **OpenAPI format**.

### Authentication

The API supports authentication with an API token with the "Web API" permission, without limited
scopes of access.

You can provision an API token [from the Settings page](https://semgrep.dev/orgs/-/settings/tokens).

### Terms of Use

Please note, the materials made available herein are subject to the
[Semgrep Terms of Use](https://semgrep.dev/resources/website-terms/), and your
access or use of any of the same is your acknowledgment and acceptance of the
such terms.

<br>


___


## Install the Package

Install the SDK by adding the following dependency in your project's pom.xml file:

```xml
<dependency>
  <groupId>io.sdks</groupId>
  <artifactId>apimatic-semgrep-sdk</artifactId>
  <version>0.0.1</version>
</dependency>
```

You can also view the package at:
https://central.sonatype.com/artifact/io.sdks/apimatic-semgrep-sdk/0.0.1

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/README.md#environments) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| httpClientConfig | [`Consumer<HttpClientConfiguration.Builder>`](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/http-client-configuration-builder.md) | Set up Http Client Configuration instance. |
| loggingConfig | [`Consumer<ApiLoggingConfiguration.Builder>`](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/api-logging-configuration-builder.md) | Set up Logging Configuration instance. |
| semgrepAdminJwtCredentials | [`SemgrepAdminJwtCredentials`](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/auth/oauth-2-bearer-token.md) | The Credentials Setter for OAuth 2 Bearer token |
| semgrepJwtCredentials | [`SemgrepJwtCredentials`](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/auth/oauth-2-bearer-token-1.md) | The Credentials Setter for OAuth 2 Bearer token |
| semgrepWebTokenCredentials | [`SemgrepWebTokenCredentials`](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/auth/oauth-2-bearer-token-2.md) | The Credentials Setter for OAuth 2 Bearer token |

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

## Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

### Fields

| Name | Description |
|  --- | --- |
| PRODUCTION | **Default** |

## Authorization

This API uses the following authentication schemes.

* [`SemgrepAdminJWT (OAuth 2 Bearer token)`](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/auth/oauth-2-bearer-token.md)
* [`SemgrepJWT (OAuth 2 Bearer token)`](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/auth/oauth-2-bearer-token-1.md)
* [`SemgrepWebToken (OAuth 2 Bearer token)`](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/auth/oauth-2-bearer-token-2.md)

## List of APIs

* [Deployments Service](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/controllers/deployments-service.md)
* [Findings Service](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/controllers/findings-service.md)
* [Misc Service](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/controllers/misc-service.md)
* [Policies Service](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/controllers/policies-service.md)
* [Projects Service](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/controllers/projects-service.md)
* [Scans Service](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/controllers/scans-service.md)
* [Secrets Service](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/controllers/secrets-service.md)
* [Supply Chain Service](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/controllers/supply-chain-service.md)
* [Ticketing Service](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/controllers/ticketing-service.md)
* [Triage Service](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/controllers/triage-service.md)

## SDK Infrastructure

### Configuration

* [ApiLoggingConfiguration](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/api-logging-configuration.md)
* [ApiLoggingConfiguration.Builder](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/api-logging-configuration-builder.md)
* [ApiRequestLoggingConfiguration.Builder](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/api-request-logging-configuration-builder.md)
* [ApiResponseLoggingConfiguration.Builder](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/api-response-logging-configuration-builder.md)
* [Configuration Interface](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/configuration-interface.md)
* [HttpClientConfiguration](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/http-client-configuration.md)
* [HttpClientConfiguration.Builder](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/http-client-configuration-builder.md)
* [HttpProxyConfiguration](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/http-proxy-configuration.md)
* [HttpProxyConfiguration.Builder](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/http-proxy-configuration-builder.md)

### HTTP

* [Headers](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/headers.md)
* [HttpCallback Interface](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/http-callback-interface.md)
* [HttpContext](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/http-context.md)
* [HttpBodyRequest](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/http-body-request.md)
* [HttpRequest](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/http-request.md)
* [HttpResponse](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/http-response.md)
* [HttpStringResponse](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/http-string-response.md)

### Utilities

* [ApiException](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/api-exception.md)
* [ApiResponse](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/api-response.md)
* [ApiHelper](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/api-helper.md)
* [FileWrapper](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/file-wrapper.md)
* [DateTimeHelper](https://www.github.com/sdks-io/apimatic-semgrep-java-sdk/tree/0.0.1/doc/date-time-helper.md)

