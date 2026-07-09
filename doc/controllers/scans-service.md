# Scans Service

View details of scans associated with projects in your organization.

```java
ScansServiceApi scansServiceApi = client.getScansServiceApi();
```

## Class Name

`ScansServiceApi`

## Methods

* [Get Scan](../../doc/controllers/scans-service.md#get-scan)
* [Search Scans](../../doc/controllers/scans-service.md#search-scans)


# Get Scan

Request the details of a scan including the associated deployment, repository, and commit information.

```java
CompletableFuture<ApiResponse<ProtosOpenapiV1GetScanResponse>> getScanAsync(
    final String deploymentId,
    final String scanId)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `String` | Template, Required | - |
| `scanId` | `String` | Template, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ProtosOpenapiV1GetScanResponse`](../../doc/models/protos-openapi-v1-get-scan-response.md).

## Example Usage

```java
String deploymentId = "123";
String scanId = "456";

scansServiceApi.getScanAsync(deploymentId, scanId).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Search Scans

List the scans associated with a particular repository over the past 30 days.

```java
CompletableFuture<ApiResponse<ProtosOpenapiV1SearchScansResponse>> searchScansAsync(
    final String deploymentId,
    final SearchScansRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `String` | Template, Required | - |
| `body` | [`SearchScansRequest`](../../doc/models/search-scans-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ProtosOpenapiV1SearchScansResponse`](../../doc/models/protos-openapi-v1-search-scans-response.md).

## Example Usage

```java
String deploymentId = "123";
SearchScansRequest body = new SearchScansRequest.Builder(
    "123"
)
.build();

scansServiceApi.searchScansAsync(deploymentId, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

