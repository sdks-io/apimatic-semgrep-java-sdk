# Supply Chain Service

Manage the Supply Chain findings and dependencies of your organization.

A request body is required, but may be an empty object.

```java
SupplyChainServiceApi supplyChainServiceApi = client.getSupplyChainServiceApi();
```

## Class Name

`SupplyChainServiceApi`

## Methods

* [Supply Chain Service List Dependencies](../../doc/controllers/supply-chain-service.md#supply-chain-service-list-dependencies)
* [Supply Chain Service List Repositories for Dependencies](../../doc/controllers/supply-chain-service.md#supply-chain-service-list-repositories-for-dependencies)
* [Supply Chain Service List Lockfiles for Dependencies](../../doc/controllers/supply-chain-service.md#supply-chain-service-list-lockfiles-for-dependencies)
* [Supply Chain Service Create Sbom Export](../../doc/controllers/supply-chain-service.md#supply-chain-service-create-sbom-export)
* [Supply Chain Service Get Sbom Export](../../doc/controllers/supply-chain-service.md#supply-chain-service-get-sbom-export)


# Supply Chain Service List Dependencies

```java
CompletableFuture<ApiResponse<ListDependenciesResponse>> supplyChainServiceListDependenciesAsync(
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

supplyChainServiceApi.supplyChainServiceListDependenciesAsync(deploymentId, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Supply Chain Service List Repositories for Dependencies

```java
CompletableFuture<ApiResponse<ListRepositoriesForDependenciesResponse>> supplyChainServiceListRepositoriesForDependenciesAsync(
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

supplyChainServiceApi.supplyChainServiceListRepositoriesForDependenciesAsync(deploymentId, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Supply Chain Service List Lockfiles for Dependencies

```java
CompletableFuture<ApiResponse<ListLockfilesForDependenciesResponse>> supplyChainServiceListLockfilesForDependenciesAsync(
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

supplyChainServiceApi.supplyChainServiceListLockfilesForDependenciesAsync(deploymentId, repositoryId, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Supply Chain Service Create Sbom Export

```java
CompletableFuture<ApiResponse<CreateSbomExportResponse>> supplyChainServiceCreateSbomExportAsync(
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

supplyChainServiceApi.supplyChainServiceCreateSbomExportAsync(deploymentId, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Supply Chain Service Get Sbom Export

```java
CompletableFuture<ApiResponse<GetSbomExportResponse>> supplyChainServiceGetSbomExportAsync(
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

supplyChainServiceApi.supplyChainServiceGetSbomExportAsync(deploymentId, taskToken).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

