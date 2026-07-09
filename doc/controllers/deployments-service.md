# Deployments Service

Deployments encapsulate your organization's security organization, with multiple projects, policies, and integrations. As the root object of the organization, they're similarly the root object of the API.

```java
DeploymentsServiceApi deploymentsServiceApi = client.getDeploymentsServiceApi();
```

## Class Name

`DeploymentsServiceApi`


# List Deployments

Request the deployments your auth can access.

Currently available auth scope does not extend over more than one deployment. This endpoint returns the single deployment your token can access. The endpoint additionally returns links to related resources available on this API.

```java
CompletableFuture<ApiResponse<ProtosOpenapiV1ListDeploymentsResponse>> listDeploymentsAsync()
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ProtosOpenapiV1ListDeploymentsResponse`](../../doc/models/protos-openapi-v1-list-deployments-response.md).

## Example Usage

```java
deploymentsServiceApi.listDeploymentsAsync().thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

