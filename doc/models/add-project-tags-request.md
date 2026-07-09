
# Add Project Tags Request

*This model accepts additional fields of type Object.*

## Structure

`AddProjectTagsRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DeploymentSlug` | `String` | Required | Slug of the deployment name. Can be found at `/deployments`, or in your Settings in the web UI. | String getDeploymentSlug() | setDeploymentSlug(String deploymentSlug) |
| `ProjectName` | `String` | Required | Name of the project, typically the repository formatted as a path. | String getProjectName() | setProjectName(String projectName) |
| `Tags` | `List<String>` | Optional | - | List<String> getTags() | setTags(List<String> tags) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.AddProjectTagsRequest;
import java.io.IOException;
import java.util.Arrays;

AddProjectTagsRequest addProjectTagsRequest = new AddProjectTagsRequest.Builder(
    "your-deployment",
    "organization/project"
)
.tags(Arrays.asList(
        "tag"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

