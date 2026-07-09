
# Protos Openapi V1 Get Scan Response

*This model accepts additional fields of type Object.*

## Structure

`ProtosOpenapiV1GetScanResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CompletedAt` | `String` | Optional | imestamp of when the scan started. | String getCompletedAt() | setCompletedAt(String completedAt) |
| `DeploymentId` | `Long` | Optional | The unique ID of the deployment associated with the scanned repository. | Long getDeploymentId() | setDeploymentId(Long deploymentId) |
| `EnabledProducts` | `List<String>` | Optional | The products used when running the scan. | List<String> getEnabledProducts() | setEnabledProducts(List<String> enabledProducts) |
| `ExitCode` | `Long` | Optional | - | Long getExitCode() | setExitCode(Long exitCode) |
| `HasLogs` | `Boolean` | Optional | - | Boolean getHasLogs() | setHasLogs(Boolean hasLogs) |
| `Id` | `Long` | Optional | The unique ID representing this scan. | Long getId() | setId(Long id) |
| `Meta` | [`ProtosOpenapiV1GetScanResponseScanMeta`](../../doc/models/protos-openapi-v1-get-scan-response-scan-meta.md) | Optional | - | ProtosOpenapiV1GetScanResponseScanMeta getMeta() | setMeta(ProtosOpenapiV1GetScanResponseScanMeta meta) |
| `RepositoryId` | `Long` | Optional | The unique ID of the repository that was scanned. | Long getRepositoryId() | setRepositoryId(Long repositoryId) |
| `StartedAt` | `String` | Optional | when the scan was started | String getStartedAt() | setStartedAt(String startedAt) |
| `Stats` | `Object` | Optional | Miscellaneous statistics about the scan, like number of findings found and scan duration. | Object getStats() | setStats(Object stats) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosOpenapiV1GetScanResponse;
import java.io.IOException;
import java.util.Arrays;

ProtosOpenapiV1GetScanResponse protosOpenapiV1GetScanResponse = new ProtosOpenapiV1GetScanResponse.Builder()
    .completedAt("2023-11-18 23:28:12.391807+00:00")
    .deploymentId(120L)
    .enabledProducts(Arrays.asList(
        "secrets"
    ))
    .exitCode(102L)
    .hasLogs(false)
    .id(123L)
    .repositoryId(1234567L)
    .startedAt("2023-11-18 23:28:12.391807+00:00")
    .stats(ApiHelper.deserialize("{\"findings\":5,\"total_time\":100}"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

