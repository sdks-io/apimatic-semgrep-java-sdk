
# Protos Scan V1 Scan Public

*This model accepts additional fields of type Object.*

## Structure

`ProtosScanV1ScanPublic`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Branch` | `String` | Optional | The scanned branch | String getBranch() | setBranch(String branch) |
| `Commit` | `String` | Optional | The commit hash that was scanned | String getCommit() | setCommit(String commit) |
| `CompletedAt` | `LocalDateTime` | Optional | The timestamp when this scan completed (if it has completed). | LocalDateTime getCompletedAt() | setCompletedAt(LocalDateTime completedAt) |
| `DeploymentId` | `String` | Optional | Unique identifier for the deployment of the scan. | String getDeploymentId() | setDeploymentId(String deploymentId) |
| `EnabledProducts` | `List<String>` | Optional | The products used when running the scan. | List<String> getEnabledProducts() | setEnabledProducts(List<String> enabledProducts) |
| `ExitCode` | `String` | Optional | The exit_code of the scan (see https://semgrep.dev/docs/cli-reference#exit-codes) | String getExitCode() | setExitCode(String exitCode) |
| `FindingsCounts` | [`ProtosScanV1ScanFindingsCounts`](../../doc/models/protos-scan-v1-scan-findings-counts.md) | Optional | - | ProtosScanV1ScanFindingsCounts getFindingsCounts() | setFindingsCounts(ProtosScanV1ScanFindingsCounts findingsCounts) |
| `Id` | `String` | Optional | ID of the scan. | String getId() | setId(String id) |
| `IsFullScan` | `Boolean` | Optional | Whether the scan was a full scan (true) or a diff scan (false) | Boolean getIsFullScan() | setIsFullScan(Boolean isFullScan) |
| `RepositoryId` | `String` | Optional | Unique identifier for the repository of the scan. | String getRepositoryId() | setRepositoryId(String repositoryId) |
| `StartedAt` | `LocalDateTime` | Optional | The timestamp when this scan started. | LocalDateTime getStartedAt() | setStartedAt(LocalDateTime startedAt) |
| `Status` | [`Status7`](../../doc/models/status-7.md) | Optional | The current status of the scan<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SCAN_STATUS_RUNNING \| The scan is currently running \|<br>\| SCAN_STATUS_COMPLETED \| The scan has completed successfully (0 or 1 exit code) \|<br>\| SCAN_STATUS_PENDING \| The scan is queued and waiting to start \|<br>\| SCAN_STATUS_CANCELLED \| The scan was cancelled before completion \|<br>\| SCAN_STATUS_ERROR \| The scan has exited with a failure (exit code not 0 or 1) \|<br>\| SCAN_STATUS_NEVER_FINISHED \| The scan did not report an error or success after over an hour \| | Status7 getStatus() | setStatus(Status7 status) |
| `TotalTime` | `Double` | Optional | Duration of scan, in seconds | Double getTotalTime() | setTotalTime(Double totalTime) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.DateTimeHelper;
import dev.semgrep.models.ProtosScanV1ScanPublic;
import dev.semgrep.models.Status7;
import java.io.IOException;
import java.util.Arrays;

ProtosScanV1ScanPublic protosScanV1ScanPublic = new ProtosScanV1ScanPublic.Builder()
    .branch("main")
    .commit("6d3de02545f820febf2af9820568fa5f697d4087")
    .completedAt(DateTimeHelper.fromRfc8601DateTime("2020-11-18 23:30:10.216670+00:00"))
    .deploymentId("deployment_id0")
    .enabledProducts(Arrays.asList(
        "secrets"
    ))
    .exitCode("0")
    .isFullScan(true)
    .startedAt(DateTimeHelper.fromRfc8601DateTime("2020-11-18 23:28:12.391807+00:00"))
    .status(Status7.SCAN_STATUS_RUNNING)
    .totalTime(17.32D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

