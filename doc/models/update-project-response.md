
# Update Project Response

Successfully updated details for the project.

*This model accepts additional fields of type Object.*

## Structure

`UpdateProjectResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Project` | [`Project`](../../doc/models/project.md) | Required | A project in your organization that uses Semgrep. | Project getProject() | setProject(Project project) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ManagedScanConfig;
import dev.semgrep.models.Project;
import dev.semgrep.models.ProtosOpenapiV1DiffScan;
import dev.semgrep.models.ProtosOpenapiV1FullScan;
import dev.semgrep.models.UpdateProjectResponse;
import java.io.IOException;
import java.util.Arrays;

UpdateProjectResponse updateProjectResponse = new UpdateProjectResponse.Builder(
    new Project.Builder(
        1234567L,
        "returntocorp/semgrep",
        Arrays.asList(
            "tag"
        )
    )
    .createdAt("2020-11-18 23:28:12.391807+00:00")
    .defaultBranch("refs/heads/main")
    .latestScanAt("2023-01-13 20:51:51.449081+00:00")
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
    .primaryBranch("refs/heads/custom-main")
    .url("https://github.com/returntocorp/semgrep")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

