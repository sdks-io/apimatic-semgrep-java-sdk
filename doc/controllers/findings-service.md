# Findings Service

Manage and retrieve code, supply chain, and AI-powered scan findings from Semgrep scans

```java
FindingsServiceApi findingsServiceApi = client.getFindingsServiceApi();
```

## Class Name

`FindingsServiceApi`


# Findings Service List Findings

Request the list of code, supply chain, or AI-powered scan findings in an organization, paginated in pages of 100 entries and limited by the `since` timestamp. Findings are returned by `relevant_since` descending (see `since` in the Query Parameters list). Examples: List SAST findings with pagination, List SCA findings since timestamp, List AI-powered scan findings, List findings with filters.

```java
CompletableFuture<ApiResponse<ApiV1DeploymentsFindingsResponse>> findingsServiceListFindingsAsync(
    final String deploymentSlug,
    final IssueType2 issueType,
    final Double since,
    final Long page,
    final Boolean dedup,
    final Long pageSize,
    final List<String> repos,
    final List<Long> repositoryIds,
    final Status9 status,
    final TriageReasons2 triageReasons,
    final Severities2 severities,
    final String ref,
    final List<String> policies,
    final List<String> rules,
    final List<String> categories,
    final Confidence8 confidence,
    final AutotriageVerdict2 autotriageVerdict,
    final List<String> componentTags,
    final Exposures2 exposures,
    final Transitivities2 transitivities,
    final Boolean isMalicious,
    final ClickToFixPrState clickToFixPrState)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `String` | Template, Required | - |
| `issueType` | [`IssueType2`](../../doc/models/issue-type-2.md) | Query, Optional | **Default**: `IssueType2.SAST` |
| `since` | `Double` | Query, Optional | - |
| `page` | `Long` | Query, Optional | **Default**: `0L` |
| `dedup` | `Boolean` | Query, Optional | **Default**: `false` |
| `pageSize` | `Long` | Query, Optional | **Default**: `100L`<br><br>**Constraints**: `>= 100`, `<= 3000` |
| `repos` | `List<String>` | Query, Optional | - |
| `repositoryIds` | `List<Long>` | Query, Optional | - |
| `status` | [`Status9`](../../doc/models/status-9.md) | Query, Optional | - |
| `triageReasons` | [`TriageReasons2`](../../doc/models/triage-reasons-2.md) | Query, Optional | - |
| `severities` | [`Severities2`](../../doc/models/severities-2.md) | Query, Optional | - |
| `ref` | `String` | Query, Optional | - |
| `policies` | `List<String>` | Query, Optional | - |
| `rules` | `List<String>` | Query, Optional | - |
| `categories` | `List<String>` | Query, Optional | - |
| `confidence` | [`Confidence8`](../../doc/models/confidence-8.md) | Query, Optional | - |
| `autotriageVerdict` | [`AutotriageVerdict2`](../../doc/models/autotriage-verdict-2.md) | Query, Optional | - |
| `componentTags` | `List<String>` | Query, Optional | - |
| `exposures` | [`Exposures2`](../../doc/models/exposures-2.md) | Query, Optional | - |
| `transitivities` | [`Transitivities2`](../../doc/models/transitivities-2.md) | Query, Optional | - |
| `isMalicious` | `Boolean` | Query, Optional | - |
| `clickToFixPrState` | [`ClickToFixPrState`](../../doc/models/click-to-fix-pr-state.md) | Query, Optional | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ApiV1DeploymentsFindingsResponse`](../../doc/models/api-v1-deployments-findings-response.md).

## Example Usage

```java
String deploymentSlug = "your-deployment";
IssueType2 issueType = IssueType2.SCA;
Double since = 1636942398.45D;
Long page = 1L;
Boolean dedup = true;
Long pageSize = 100L;
List<String> repos = Arrays.asList(
    "myorg/repo1",
    "myorg/repo2"
);

List<Long> repositoryIds = Arrays.asList(
    1L,
    2L,
    3L
);

Status9 status = Status9.OPEN;
String ref = "refs/pull/1234/merge";
List<String> policies = Arrays.asList(
    "rule-board-block",
    "rule-board-pr-comments",
    "rule-board-audit"
);

List<String> rules = Arrays.asList(
    "typescript.react.security.audit.react-no-refs.react-no-refs",
    "ajinabraham.njsscan.hardcoded_secrets.node_username"
);

List<String> categories = Arrays.asList(
    "security",
    "correctness",
    "caching"
);

Confidence8 confidence = Confidence8.HIGH;
AutotriageVerdict2 autotriageVerdict = AutotriageVerdict2.TRUE_POSITIVE;
List<String> componentTags = Arrays.asList(
    "user authentication",
    "user data"
);

Boolean isMalicious = true;

findingsServiceApi.findingsServiceListFindingsAsync(deploymentSlug, issueType, since, page, dedup, pageSize, repos, repositoryIds, status, null, null, ref, policies, rules, categories, confidence, autotriageVerdict, componentTags, null, null, isMalicious, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

