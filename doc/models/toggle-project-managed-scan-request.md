
# Toggle Project Managed Scan Request

*This model accepts additional fields of type Object.*

## Structure

`ToggleProjectManagedScanRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeploymentSlug` | `String` | Required | Slug of the deployment name. Can be found at `/deployments`, or in your Settings in the web UI. | String getDeploymentSlug() | setDeploymentSlug(String deploymentSlug) |
| `DiffScan` | [`ProtosOpenapiV1DiffScan`](../../doc/models/protos-openapi-v1-diff-scan.md) | Optional | - | ProtosOpenapiV1DiffScan getDiffScan() | setDiffScan(ProtosOpenapiV1DiffScan diffScan) |
| `FullScan` | [`ProtosOpenapiV1FullScan`](../../doc/models/protos-openapi-v1-full-scan.md) | Optional | - | ProtosOpenapiV1FullScan getFullScan() | setFullScan(ProtosOpenapiV1FullScan fullScan) |
| `ProjectName` | `String` | Required | Name of the project, typically the repository formatted as a path. | String getProjectName() | setProjectName(String projectName) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosOpenapiV1DiffScan;
import dev.semgrep.models.ProtosOpenapiV1FullScan;
import dev.semgrep.models.ToggleProjectManagedScanRequest;
import java.io.IOException;

ToggleProjectManagedScanRequest toggleProjectManagedScanRequest = new ToggleProjectManagedScanRequest.Builder(
    "your-deployment",
    "organization/project"
)
.diffScan(new ProtosOpenapiV1DiffScan.Builder()
        .enabled(false)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.fullScan(new ProtosOpenapiV1FullScan.Builder()
        .enabled(false)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

