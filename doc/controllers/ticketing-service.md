# Ticketing Service

Create and manage external tickets

```java
TicketingServiceApi ticketingServiceApi = client.getTicketingServiceApi();
```

## Class Name

`TicketingServiceApi`

## Methods

* [Delete Ticket](../../doc/controllers/ticketing-service.md#delete-ticket)
* [Link Ticket](../../doc/controllers/ticketing-service.md#link-ticket)
* [Unlink Ticket](../../doc/controllers/ticketing-service.md#unlink-ticket)
* [Create Ticket](../../doc/controllers/ticketing-service.md#create-ticket)


# Delete Ticket

Unlink a Jira ticket by its ID

```java
CompletableFuture<ApiResponse<ProtosOpenapiV1DeleteTicketResponse>> deleteTicketAsync(
    final String deploymentId,
    final long externalTicketId)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `String` | Template, Required | - |
| `externalTicketId` | `long` | Template, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ProtosOpenapiV1DeleteTicketResponse`](../../doc/models/protos-openapi-v1-delete-ticket-response.md).

## Example Usage

```java
String deploymentId = "123";
long externalTicketId = 456L;

ticketingServiceApi.deleteTicketAsync(deploymentId, externalTicketId).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Link Ticket

Link an existing external ticket (e.g. Jira) to one or more Semgrep findings by providing the ticket URL and a list of finding IDs. This does not create a ticket in your issue tracker — it only records the association in Semgrep. If a finding is already linked to a different ticket, the existing link is replaced. Requires a configured ticketing integration.

```java
CompletableFuture<ApiResponse<ProtosOpenapiV1LinkTicketResponse>> linkTicketAsync(
    final String deploymentId,
    final LinkTicketRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `String` | Template, Required | - |
| `body` | [`LinkTicketRequest`](../../doc/models/link-ticket-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ProtosOpenapiV1LinkTicketResponse`](../../doc/models/protos-openapi-v1-link-ticket-response.md).

## Example Usage

```java
String deploymentId = "123";
LinkTicketRequest body = new LinkTicketRequest.Builder(
    "123",
    Arrays.asList(
        "issue_ids0",
        "issue_ids9"
    ),
    "https://myorg.atlassian.net/browse/SEC-123"
)
.build();

ticketingServiceApi.linkTicketAsync(deploymentId, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Unlink Ticket

Remove the ticket association from one or more Semgrep findings by providing a list of finding IDs. This does not delete the ticket in your issue tracker — it only removes the association in Semgrep.

```java
CompletableFuture<ApiResponse<ProtosOpenapiV1UnlinkTicketResponse>> unlinkTicketAsync(
    final String deploymentId,
    final UnlinkTicketRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `String` | Template, Required | - |
| `body` | [`UnlinkTicketRequest`](../../doc/models/unlink-ticket-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ProtosOpenapiV1UnlinkTicketResponse`](../../doc/models/protos-openapi-v1-unlink-ticket-response.md).

## Example Usage

```java
String deploymentId = "123";
UnlinkTicketRequest body = new UnlinkTicketRequest.Builder(
    "123",
    Arrays.asList(
        "issue_ids0",
        "issue_ids9"
    )
)
.build();

ticketingServiceApi.unlinkTicketAsync(deploymentId, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Create Ticket

Create Jira tickets for your findings. You can create tickets by passing in a list of issue_ids or by passing in filter query parameters to dynamically select findings. If passing in filters, Semgrep will skip already ticketed findings. This endpoint is synchronous, so it may take some time for your request to resolve. Unlike creating tickets in-app, if ticket creation fails we won't automatically retry. This endpoint accepts a limit parameter (defaulting to 20) to limit the number of tickets created per request. If you specify a list of issue_ids greater than this limit, or your selected filters match on a number of issues greater than this limit, issues that were not ticketed are included in the Failed part of the response object. You can send another request to create tickets for these skipped issues. By default, findings belonging to the same repository and the same rule will be grouped together into a single Jira ticket. You can override this using the group_issues query parameter. Up to 50 issues can be grouped into a single ticket. You can optionally override the Jira project you create tickets in by passing in a Jira project ID as jira_project_id (the numeric ID rather than the project key). You can fetch this ID using the Jira API.

```java
CompletableFuture<ApiResponse<ProtosOpenapiV1CreateTicketResponse>> createTicketAsync(
    final String deploymentSlug,
    final CreateTicketRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `String` | Template, Required | - |
| `body` | [`CreateTicketRequest`](../../doc/models/create-ticket-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ProtosOpenapiV1CreateTicketResponse`](../../doc/models/protos-openapi-v1-create-ticket-response.md).

## Example Usage

```java
String deploymentSlug = "deploymentSlug6";
CreateTicketRequest body = new CreateTicketRequest.Builder(
    "deploymentSlug2",
    IssueType1.SCA
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
.groupIssues(true)
.includeHistorical(true)
.issueIds(Arrays.asList(
        "issue_ids6",
        "issue_ids7"
    ))
.jiraProjectId("12345")
.limit(20L)
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

ticketingServiceApi.createTicketAsync(deploymentSlug, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

