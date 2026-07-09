# Projects Service

```java
ProjectsServiceApi projectsServiceApi = client.getProjectsServiceApi();
```

## Class Name

`ProjectsServiceApi`

## Methods

* [Projects Service List Projects](../../doc/controllers/projects-service.md#projects-service-list-projects)
* [Projects Service Delete Project](../../doc/controllers/projects-service.md#projects-service-delete-project)
* [Projects Service Get Project](../../doc/controllers/projects-service.md#projects-service-get-project)
* [Projects Service Update Project](../../doc/controllers/projects-service.md#projects-service-update-project)
* [Projects Service Toggle Project Managed Scan](../../doc/controllers/projects-service.md#projects-service-toggle-project-managed-scan)
* [Projects Service Delete Project Tags](../../doc/controllers/projects-service.md#projects-service-delete-project-tags)
* [Projects Service Add Project Tags](../../doc/controllers/projects-service.md#projects-service-add-project-tags)


# Projects Service List Projects

Request the list of projects that have been scanned or onboarded to Managed Scans. Does not return archived repositories. Returns 100 projects per page by default.

```java
CompletableFuture<ApiResponse<ListProjectsResponse>> projectsServiceListProjectsAsync(
    final String deploymentSlug,
    final Long page,
    final Long pageSize)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `String` | Template, Required | - |
| `page` | `Long` | Query, Optional | - |
| `pageSize` | `Long` | Query, Optional | **Default**: `100L` |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ListProjectsResponse`](../../doc/models/list-projects-response.md).

## Example Usage

```java
String deploymentSlug = "your-deployment";
Long page = 1L;
Long pageSize = 100L;

projectsServiceApi.projectsServiceListProjectsAsync(deploymentSlug, page, pageSize).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Projects Service Delete Project

Delete a project for a deployment you have access to. This will also delete all of the associated findings.

```java
CompletableFuture<ApiResponse<DeleteProjectResponse>> projectsServiceDeleteProjectAsync(
    final String deploymentSlug,
    final String projectName)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `String` | Template, Required | - |
| `projectName` | `String` | Template, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`DeleteProjectResponse`](../../doc/models/delete-project-response.md).

## Example Usage

```java
String deploymentSlug = "your-deployment";
String projectName = "organization/project";

projectsServiceApi.projectsServiceDeleteProjectAsync(deploymentSlug, projectName).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Projects Service Get Project

Retrieve details for a single project associated with a deployment that you have access to.

```java
CompletableFuture<ApiResponse<GetProjectResponse>> projectsServiceGetProjectAsync(
    final String deploymentSlug,
    final String projectName)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `String` | Template, Required | - |
| `projectName` | `String` | Template, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`GetProjectResponse`](../../doc/models/get-project-response.md).

## Example Usage

```java
String deploymentSlug = "your-deployment";
String projectName = "organization/project";

projectsServiceApi.projectsServiceGetProjectAsync(deploymentSlug, projectName).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Projects Service Update Project

Update attributes for the project using the value passed in to the request body.

Note: The only attribute that is supported as of January 2023 is `tags`.

```java
CompletableFuture<ApiResponse<UpdateProjectResponse>> projectsServiceUpdateProjectAsync(
    final String deploymentSlug,
    final String projectName,
    final UpdateProjectRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `String` | Template, Required | - |
| `projectName` | `String` | Template, Required | - |
| `body` | [`UpdateProjectRequest`](../../doc/models/update-project-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`UpdateProjectResponse`](../../doc/models/update-project-response.md).

## Example Usage

```java
String deploymentSlug = "your-deployment";
String projectName = "organization/project";
UpdateProjectRequest body = new UpdateProjectRequest.Builder(
    "your-deployment",
    "organization/project"
)
.primaryBranch("refs/heads/develop")
.tags(Arrays.asList(
        "tag"
    ))
.build();

projectsServiceApi.projectsServiceUpdateProjectAsync(deploymentSlug, projectName, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Projects Service Toggle Project Managed Scan

Enable or disable
[Semgrep Managed Scans](/docs/deployment/managed-scanning/overview)
for a project.

```java
CompletableFuture<ApiResponse<ToggleProjectManagedScanResponse>> projectsServiceToggleProjectManagedScanAsync(
    final String deploymentSlug,
    final String projectName,
    final ToggleProjectManagedScanRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `String` | Template, Required | - |
| `projectName` | `String` | Template, Required | - |
| `body` | [`ToggleProjectManagedScanRequest`](../../doc/models/toggle-project-managed-scan-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ToggleProjectManagedScanResponse`](../../doc/models/toggle-project-managed-scan-response.md).

## Example Usage

```java
String deploymentSlug = "your-deployment";
String projectName = "organization/project";
ToggleProjectManagedScanRequest body = new ToggleProjectManagedScanRequest.Builder(
    "your-deployment",
    "organization/project"
)
.build();

projectsServiceApi.projectsServiceToggleProjectManagedScanAsync(deploymentSlug, projectName, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Projects Service Delete Project Tags

Remove tags from a project for a deployment you have access to.

This request will not delete project tags from the deployment and will only remove
them from the requested project. Any other projects associated with the requested
tag will remain unaffected.

```java
CompletableFuture<ApiResponse<DeleteProjectTagsResponse>> projectsServiceDeleteProjectTagsAsync(
    final String deploymentSlug,
    final String projectName,
    final List<String> tags)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `String` | Template, Required | - |
| `projectName` | `String` | Template, Required | - |
| `tags` | `List<String>` | Query, Optional | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`DeleteProjectTagsResponse`](../../doc/models/delete-project-tags-response.md).

## Example Usage

```java
String deploymentSlug = "your-deployment";
String projectName = "organization/project";
List<String> tags = Arrays.asList(
    "tag"
);

projectsServiceApi.projectsServiceDeleteProjectTagsAsync(deploymentSlug, projectName, tags).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Projects Service Add Project Tags

Add tags to a project for a deployment you have access to.

Any project tags that do not already exist for the deployment will be created automatically and associated with the project.

```java
CompletableFuture<ApiResponse<AddProjectTagsResponse>> projectsServiceAddProjectTagsAsync(
    final String deploymentSlug,
    final String projectName,
    final AddProjectTagsRequest body)
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `String` | Template, Required | - |
| `projectName` | `String` | Template, Required | - |
| `body` | [`AddProjectTagsRequest`](../../doc/models/add-project-tags-request.md) | Body, Required | - |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`AddProjectTagsResponse`](../../doc/models/add-project-tags-response.md).

## Example Usage

```java
String deploymentSlug = "your-deployment";
String projectName = "organization/project";
AddProjectTagsRequest body = new AddProjectTagsRequest.Builder(
    "your-deployment",
    "organization/project"
)
.tags(Arrays.asList(
        "tag"
    ))
.build();

projectsServiceApi.projectsServiceAddProjectTagsAsync(deploymentSlug, projectName, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```

