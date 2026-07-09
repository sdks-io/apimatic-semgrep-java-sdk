# Supply Chain Service

Manage the Supply Chain findings and dependencies of your organization.

A request body is required, but may be an empty object.

```java
SupplyChainServiceApi supplyChainServiceApi = client.getSupplyChainServiceApi();
```

## Class Name

`SupplyChainServiceApi`

## Methods

* [List Dependencies](../../doc/controllers/supply-chain-service.md#list-dependencies)
* [List Repositories for Dependencies](../../doc/controllers/supply-chain-service.md#list-repositories-for-dependencies)
* [List Lockfiles for Dependencies](../../doc/controllers/supply-chain-service.md#list-lockfiles-for-dependencies)
* [Create Sbom Export](../../doc/controllers/supply-chain-service.md#create-sbom-export)
* [Get Sbom Export](../../doc/controllers/supply-chain-service.md#get-sbom-export)


# List Dependencies

```java
CompletableFuture<ApiResponse<ListDependenciesResponse>> listDependenciesAsync(
    final String deploymentId,
    final ListDependenciesRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `String` | Template, Required | - |
| `body` | [`ListDependenciesRequest`](../../doc/models/list-dependencies-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ListDependenciesResponse`](../../doc/models/list-dependencies-response.md).

## Example Usage

```java
String deploymentId = "123";
ListDependenciesRequest body = new ListDependenciesRequest.Builder(
    "123"
)
.pageSize(1000L)
.build();

supplyChainServiceApi.listDependenciesAsync(deploymentId, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# List Repositories for Dependencies

```java
CompletableFuture<ApiResponse<ListRepositoriesForDependenciesResponse>> listRepositoriesForDependenciesAsync(
    final String deploymentId,
    final ListRepositoriesForDependenciesRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `String` | Template, Required | - |
| `body` | [`ListRepositoriesForDependenciesRequest`](../../doc/models/list-repositories-for-dependencies-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ListRepositoriesForDependenciesResponse`](../../doc/models/list-repositories-for-dependencies-response.md).

## Example Usage

```java
String deploymentId = "deploymentId2";
ListRepositoriesForDependenciesRequest body = new ListRepositoriesForDependenciesRequest.Builder(
    "deploymentId8"
)
.pageSize(100L)
.build();

supplyChainServiceApi.listRepositoriesForDependenciesAsync(deploymentId, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# List Lockfiles for Dependencies

```java
CompletableFuture<ApiResponse<ListLockfilesForDependenciesResponse>> listLockfilesForDependenciesAsync(
    final String deploymentId,
    final String repositoryId,
    final ListLockfilesForDependenciesRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `String` | Template, Required | - |
| `repositoryId` | `String` | Template, Required | - |
| `body` | [`ListLockfilesForDependenciesRequest`](../../doc/models/list-lockfiles-for-dependencies-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ListLockfilesForDependenciesResponse`](../../doc/models/list-lockfiles-for-dependencies-response.md).

## Example Usage

```java
String deploymentId = "deploymentId2";
String repositoryId = "repositoryId6";
ListLockfilesForDependenciesRequest body = new ListLockfilesForDependenciesRequest.Builder(
    "deploymentId8",
    "repositoryId0"
)
.pageSize(100L)
.build();

supplyChainServiceApi.listLockfilesForDependenciesAsync(deploymentId, repositoryId, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Create Sbom Export

```java
CompletableFuture<ApiResponse<CreateSbomExportResponse>> createSbomExportAsync(
    final String deploymentId,
    final CreateSbomExportRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `String` | Template, Required | - |
| `body` | [`CreateSbomExportRequest`](../../doc/models/create-sbom-export-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`CreateSbomExportResponse`](../../doc/models/create-sbom-export-response.md).

## Example Usage

```java
String deploymentId = "123";
CreateSbomExportRequest body = new CreateSbomExportRequest.Builder(
    "123"
)
.metadataComponentType(MetadataComponentType.SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_APPLICATION)
.ref("refs/pull/1234/merge")
.repositoryId("123")
.sbomOutputFormat(SbomOutputFormat.SBOM_OUTPUT_FORMAT_JSON)
.build();

supplyChainServiceApi.createSbomExportAsync(deploymentId, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Get Sbom Export

```java
CompletableFuture<ApiResponse<GetSbomExportResponse>> getSbomExportAsync(
    final String deploymentId,
    final String taskToken)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `String` | Template, Required | - |
| `taskToken` | `String` | Template, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`GetSbomExportResponse`](../../doc/models/get-sbom-export-response.md).

## Example Usage

```java
String deploymentId = "123";
String taskToken = "taskToken2";

supplyChainServiceApi.getSbomExportAsync(deploymentId, taskToken).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

