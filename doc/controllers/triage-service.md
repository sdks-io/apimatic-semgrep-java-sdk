# Triage Service

View and manage the triage of your organization.

```java
TriageServiceApi triageServiceApi = client.getTriageServiceApi();
```

## Class Name

`TriageServiceApi`


# Triage Service Bulk Triage

Bulk triage your findings. You can select the findings to triage by passing in a list of finding IDs as issue_ids, or by passing in filter query parameters. You must specify the issue_type of the findings you want to bulk triage. One of new_triage_state or new_note is required. If specifying a new_triage_reason, you must also use new_triage_state=ignored. Some filters only apply for findings associated with a given product.

```java
CompletableFuture<ApiResponse<BulkTriageResponse>> triageServiceBulkTriageAsync(
    final String deploymentSlug,
    final BulkTriageRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `String` | Template, Required | - |
| `body` | [`BulkTriageRequest`](../../doc/models/bulk-triage-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`BulkTriageResponse`](../../doc/models/bulk-triage-response.md).

## Example Usage

```java
String deploymentSlug = "deploymentSlug6";
BulkTriageRequest body = new BulkTriageRequest.Builder(
    IssueType.SCA
)
.autotriageVerdict(AutotriageVerdict.TRUE_POSITIVE)
.categories(Arrays.asList(
        "security",
        "performance"
    ))
.componentTags(Arrays.asList(
        "user authentication",
        "user data"
    ))
.confidence(Confidence3.HIGH)
.dependencies(Arrays.asList(
        "lodash",
        "express"
    ))
.includeHistorical(true)
.issueIds(Arrays.asList(
        123L,
        456L
    ))
.limit(100L)
.newNote("some note here")
.newTriageReason(NewTriageReason.ACCEPTABLE_RISK)
.newTriageState(NewTriageState.REOPENED)
.policies(Arrays.asList(
        "rule-board-block",
        "rule-board-pr-comments",
        "rule-board-audit"
    ))
.proOnly(true)
.projectTags(Arrays.asList(
        "my_project_tag_1",
        "my_project_tag_2"
    ))
.ref("refs/pull/1234/merge")
.repos(Arrays.asList(
        "myorg/repo1",
        "myorg/repo2"
    ))
.rules(Arrays.asList(
        "typescript.react.security.audit.react-no-refs.react-no-refs",
        "ajinabraham.njsscan.hardcoded_secrets.node_username"
    ))
.ruleset(Arrays.asList(
        "owasp-top-ten",
        "default"
    ))
.secretTypes(Arrays.asList(
        "Github",
        "Heroku",
        "AWS"
    ))
.since("1717334400")
.status(Status1.OPEN)
.build();

triageServiceApi.triageServiceBulkTriageAsync(deploymentSlug, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

