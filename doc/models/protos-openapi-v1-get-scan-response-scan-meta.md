
# Protos Openapi V1 Get Scan Response Scan Meta

*This model accepts additional fields of type Object.*

## Structure

`ProtosOpenapiV1GetScanResponseScanMeta`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `True` | `String` | Optional | What triggered this scan, if applicable. | String getTrue() | setTrue(String mTrue) |
| `Branch` | `String` | Optional | The branch that was scanned, if applicable. | String getBranch() | setBranch(String branch) |
| `Commit` | `String` | Optional | The commit SHA associated with the scan, if applicable. | String getCommit() | setCommit(String commit) |
| `Config` | `String` | Optional | The path of the configuration file used for this scan, if applicable. | String getConfig() | setConfig(String config) |
| `RepoUrl` | `String` | Optional | The URL of the scanned repository, if applicable. | String getRepoUrl() | setRepoUrl(String repoUrl) |
| `CiJobUrl` | `String` | Optional | The URL of the CI job that ran the scan, if applicable. | String getCiJobUrl() | setCiJobUrl(String ciJobUrl) |
| `Repository` | `String` | Optional | The name and organization of the scanned repository, if applicable. | String getRepository() | setRepository(String repository) |
| `CommitTitle` | `String` | Optional | The commit message associated with the scan, if applicable. | String getCommitTitle() | setCommitTitle(String commitTitle) |
| `PullRequestId` | `String` | Optional | The ID of the pull request associated with the scan, if applicable. | String getPullRequestId() | setPullRequestId(String pullRequestId) |
| `PullRequestTitle` | `String` | Optional | The title of the pull request associated with the scan if applicable. | String getPullRequestTitle() | setPullRequestTitle(String pullRequestTitle) |
| `CommitAuthorName` | `String` | Optional | The name of the author of the commit associated with the scan, if applicable. | String getCommitAuthorName() | setCommitAuthorName(String commitAuthorName) |
| `CommitAuthorImageUrl` | `String` | Optional | The avatar image url of the author of the commit associated with the scan, if applicable. | String getCommitAuthorImageUrl() | setCommitAuthorImageUrl(String commitAuthorImageUrl) |
| `CommitAuthorEmail` | `String` | Optional | The email of the author of the commit associated with the scan, if applicable. | String getCommitAuthorEmail() | setCommitAuthorEmail(String commitAuthorEmail) |
| `CommitAuthorUsername` | `String` | Optional | The username of the author of the commit associated with the scan, if applicable. | String getCommitAuthorUsername() | setCommitAuthorUsername(String commitAuthorUsername) |
| `PullRequestAuthorUsername` | `String` | Optional | The username of the author of the pull request associated with the scan, if applicable. | String getPullRequestAuthorUsername() | setPullRequestAuthorUsername(String pullRequestAuthorUsername) |
| `PullRequestAuthorImageUrl` | `String` | Optional | The avatar image url of the author of the pull request associated with the scan, if applicable. | String getPullRequestAuthorImageUrl() | setPullRequestAuthorImageUrl(String pullRequestAuthorImageUrl) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosOpenapiV1GetScanResponseScanMeta;
import java.io.IOException;

ProtosOpenapiV1GetScanResponseScanMeta protosOpenapiV1GetScanResponseScanMeta = new ProtosOpenapiV1GetScanResponseScanMeta.Builder()
    .mTrue("pull_request")
    .branch("refs/heads/main")
    .commit("94c5be1312a9da03b7c4bfcc1c50b4379c83412")
    .config("r/python")
    .repoUrl("https://github.com/semgrep/semgrep")
    .ciJobUrl("https://github.com/semgrep/semgrep/actions/runs/12345")
    .repository("semgrep/semgrep")
    .commitTitle("{\r\n  \"fix(feature)\": \"Added XYZ component\"\r\n}")
    .pullRequestId("12345")
    .pullRequestTitle("{\r\n  \"fix(feature)\": \"Added XYZ component\"\r\n}")
    .commitAuthorName("Sven Greppe")
    .commitAuthorImageUrl("https://github.com/link/to/avatar.png")
    .commitAuthorEmail("sven.greppe@semgrep.com")
    .commitAuthorUsername("SvenGreppe")
    .pullRequestAuthorUsername("SvenGreppe")
    .pullRequestAuthorImageUrl("https://github.com/link/to/avatar.png")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

