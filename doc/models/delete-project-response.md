
# Delete Project Response

Successfully deleted the project.

*This model accepts additional fields of type Object.*

## Structure

`DeleteProjectResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ProjectName` | `String` | Required | The name of the deleted project. | String getProjectName() | setProjectName(String projectName) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.DeleteProjectResponse;
import java.io.IOException;

DeleteProjectResponse deleteProjectResponse = new DeleteProjectResponse.Builder(
    "organization/project"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

