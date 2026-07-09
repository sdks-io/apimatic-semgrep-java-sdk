
# Update Project Request

*This model accepts additional fields of type Object.*

## Structure

`UpdateProjectRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeploymentSlug` | `String` | Required | Slug of the deployment name. Can be found at `/deployments`, or in your Settings in the web UI. | String getDeploymentSlug() | setDeploymentSlug(String deploymentSlug) |
| `ManagedScanConfig` | [`ManagedScanConfig`](../../doc/models/managed-scan-config.md) | Optional | [Beta] Configuration of Semgrep Managed Scans for the project, if relevant. | ManagedScanConfig getManagedScanConfig() | setManagedScanConfig(ManagedScanConfig managedScanConfig) |
| `PrimaryBranch` | `String` | Optional | The full name of the branch you would like to set as primary. Use "None" if default_branch is known and you wish to set primary to always be the default branch. | String getPrimaryBranch() | setPrimaryBranch(String primaryBranch) |
| `ProjectName` | `String` | Required | Name of the project, typically the repository formatted as a path. | String getProjectName() | setProjectName(String projectName) |
| `Tags` | `List<String>` | Optional | Tags associated to this project. | List<String> getTags() | setTags(List<String> tags) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ManagedScanConfig;
import dev.semgrep.models.ProtosOpenapiV1DiffScan;
import dev.semgrep.models.ProtosOpenapiV1FullScan;
import dev.semgrep.models.UpdateProjectRequest;
import java.io.IOException;
import java.util.Arrays;

UpdateProjectRequest updateProjectRequest = new UpdateProjectRequest.Builder(
    "your-deployment",
    "organization/project"
)
.managedScanConfig(new ManagedScanConfig.Builder()
        .diffScan(new ProtosOpenapiV1DiffScan.Builder()
            .enabled(false)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .fullScan(new ProtosOpenapiV1FullScan.Builder()
            .enabled(false)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.primaryBranch("refs/heads/develop")
.tags(Arrays.asList(
        "tag"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

