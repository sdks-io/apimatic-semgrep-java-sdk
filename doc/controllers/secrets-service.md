# Secrets Service

View and manage the Secrets of your organization.

```java
SecretsServiceApi secretsServiceApi = client.getSecretsServiceApi();
```

## Class Name

`SecretsServiceApi`


# Secrets Service List Secrets Path

```java
CompletableFuture<ApiResponse<ProtosOpenapiV1ListSecretsPathResponse>> secretsServiceListSecretsPathAsync(
    final String deploymentId,
    final String cursor,
    final Long limit,
    final LocalDateTime since,
    final List<ValidationState3> validationState,
    final Status8 status,
    final List<Severity5> severity,
    final List<String> repo)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `String` | Template, Required | - |
| `cursor` | `String` | Query, Optional | - |
| `limit` | `Long` | Query, Optional | - |
| `since` | `LocalDateTime` | Query, Optional | - |
| `validationState` | [`List<ValidationState3>`](../../doc/models/validation-state-3.md) | Query, Optional | - |
| `status` | [`Status8`](../../doc/models/status-8.md) | Query, Optional | **Default**: `Status8.FINDING_STATUS_UNSPECIFIED` |
| `severity` | [`List<Severity5>`](../../doc/models/severity-5.md) | Query, Optional | - |
| `repo` | `List<String>` | Query, Optional | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ProtosOpenapiV1ListSecretsPathResponse`](../../doc/models/protos-openapi-v1-list-secrets-path-response.md).

## Example Usage

```java
String deploymentId = "123";
Status8 status = Status8.FINDING_STATUS_UNSPECIFIED;
secretsServiceApi.secretsServiceListSecretsPathAsync(deploymentId, null, null, null, null, status, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

