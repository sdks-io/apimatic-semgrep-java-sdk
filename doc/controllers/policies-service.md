# Policies Service

View and manage the Policies of your organization.

```java
PoliciesServiceApi policiesServiceApi = client.getPoliciesServiceApi();
```

## Class Name

`PoliciesServiceApi`

## Methods

* [List Policies](../../doc/controllers/policies-service.md#list-policies)
* [List Policy Rules](../../doc/controllers/policies-service.md#list-policy-rules)
* [Update Policy](../../doc/controllers/policies-service.md#update-policy)


# List Policies

```java
CompletableFuture<ApiResponse<ProtosOpenapiV1ListPoliciesResponse>> listPoliciesAsync(
    final String deploymentId)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `String` | Template, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ProtosOpenapiV1ListPoliciesResponse`](../../doc/models/protos-openapi-v1-list-policies-response.md).

## Example Usage

```java
String deploymentId = "123";

policiesServiceApi.listPoliciesAsync(deploymentId).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# List Policy Rules

```java
CompletableFuture<ApiResponse<ProtosOpenapiV1ListPolicyRulesResponse>> listPolicyRulesAsync(
    final String deploymentId,
    final String policyId,
    final String cursor,
    final Long limit)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `String` | Template, Required | - |
| `policyId` | `String` | Template, Required | - |
| `cursor` | `String` | Query, Optional | - |
| `limit` | `Long` | Query, Optional | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ProtosOpenapiV1ListPolicyRulesResponse`](../../doc/models/protos-openapi-v1-list-policy-rules-response.md).

## Example Usage

```java
String deploymentId = "123";
String policyId = "456";

policiesServiceApi.listPolicyRulesAsync(deploymentId, policyId, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Update Policy

```java
CompletableFuture<ApiResponse<ProtosOpenapiV1UpdatePolicyResponse>> updatePolicyAsync(
    final String deploymentId,
    final String policyId,
    final UpdatePolicyRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `String` | Template, Required | - |
| `policyId` | `String` | Template, Required | - |
| `body` | [`UpdatePolicyRequest`](../../doc/models/update-policy-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ProtosOpenapiV1UpdatePolicyResponse`](../../doc/models/protos-openapi-v1-update-policy-response.md).

## Example Usage

```java
String deploymentId = "123";
String policyId = "456";
UpdatePolicyRequest body = new UpdatePolicyRequest.Builder(
    "123",
    "456",
    PolicyMode3.MODE_BLOCK,
    "rulePath2"
)
.build();

policiesServiceApi.updatePolicyAsync(deploymentId, policyId, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

