# Policies Service

View and manage the Policies of your organization.

```java
PoliciesServiceApi policiesServiceApi = client.getPoliciesServiceApi();
```

## Class Name

`PoliciesServiceApi`

## Methods

* [Policies Service List Policies](../../doc/controllers/policies-service.md#policies-service-list-policies)
* [Policies Service List Policy Rules](../../doc/controllers/policies-service.md#policies-service-list-policy-rules)
* [Policies Service Update Policy](../../doc/controllers/policies-service.md#policies-service-update-policy)


# Policies Service List Policies

```java
CompletableFuture<ApiResponse<ProtosOpenapiV1ListPoliciesResponse>> policiesServiceListPoliciesAsync(
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

policiesServiceApi.policiesServiceListPoliciesAsync(deploymentId).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Policies Service List Policy Rules

```java
CompletableFuture<ApiResponse<ProtosOpenapiV1ListPolicyRulesResponse>> policiesServiceListPolicyRulesAsync(
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

policiesServiceApi.policiesServiceListPolicyRulesAsync(deploymentId, policyId, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Policies Service Update Policy

```java
CompletableFuture<ApiResponse<ProtosOpenapiV1UpdatePolicyResponse>> policiesServiceUpdatePolicyAsync(
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

policiesServiceApi.policiesServiceUpdatePolicyAsync(deploymentId, policyId, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

