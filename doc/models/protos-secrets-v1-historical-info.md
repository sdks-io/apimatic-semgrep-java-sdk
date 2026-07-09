
# Protos Secrets V1 Historical Info

*This model accepts additional fields of type Object.*

## Structure

`ProtosSecretsV1HistoricalInfo`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `GitBlob` | `String` | Optional | Git blob at which the finding is present. Sent in addition to the commit<br>since some SCMs have permalinks which use the blob sha, so this information<br>is useful when generating links back to the SCM. | String getGitBlob() | setGitBlob(String gitBlob) |
| `GitCommit` | `String` | Optional | Git commit at which the finding is present. Used by "historical" scans,<br>which scan non-HEAD commits in the git history. Relevant for finding, e.g.,<br>secrets which are buried in the git history which we wouldn't find at HEAD | String getGitCommit() | setGitCommit(String gitCommit) |
| `GitCommitTimestamp` | `LocalDateTime` | Optional | - | LocalDateTime getGitCommitTimestamp() | setGitCommitTimestamp(LocalDateTime gitCommitTimestamp) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.DateTimeHelper;
import dev.semgrep.models.ProtosSecretsV1HistoricalInfo;
import java.io.IOException;

ProtosSecretsV1HistoricalInfo protosSecretsV1HistoricalInfo = new ProtosSecretsV1HistoricalInfo.Builder()
    .gitBlob("gitBlob8")
    .gitCommit("gitCommit2")
    .gitCommitTimestamp(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

