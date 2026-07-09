# Misc Service

Utility endpoints.

```java
MiscServiceApi miscServiceApi = client.getMiscServiceApi();
```

## Class Name

`MiscServiceApi`

## Methods

* [Misc Service Get Bootstrap Sms Vpc](../../doc/controllers/misc-service.md#misc-service-get-bootstrap-sms-vpc)
* [Misc Service Ping](../../doc/controllers/misc-service.md#misc-service-ping)


# Misc Service Get Bootstrap Sms Vpc

VPC support for Managed Scans is in private beta.

Returns the Managed Scans VPC Bootstrap CloudFormation template in JSON format for setting up cross-account infrastructure.

This template creates IAM roles and policies needed for Semgrep Managed Scanning (SMS) VPC infrastructure automation,
including the semgrep-sms-vpc-automation role and EC2 Image Builder distribution roles for gVisor container runtime.

See the original AWS cloudformation template format at https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-formats.html

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<ProtosOpenapiV1GetBootstrapSmsVpcResponse>> miscServiceGetBootstrapSmsVpcAsync()
```

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ProtosOpenapiV1GetBootstrapSmsVpcResponse`](../../doc/models/protos-openapi-v1-get-bootstrap-sms-vpc-response.md).

## Example Usage

```java
miscServiceApi.miscServiceGetBootstrapSmsVpcAsync().thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Misc Service Ping

Use to ping the server and assert liveness.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<Object>> miscServicePingAsync()
```

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type `Object`.

## Example Usage

```java
miscServiceApi.miscServicePingAsync().thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

