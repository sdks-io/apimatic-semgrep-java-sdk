
# List Projects Response

Return the list of projects in an organization.

*This model accepts additional fields of type Object.*

## Structure

`ListProjectsResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Projects` | [`List<ListProject>`](../../doc/models/list-project.md) | Required | - | List<ListProject> getProjects() | setProjects(List<ListProject> projects) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ListProject;
import dev.semgrep.models.ListProjectsResponse;
import java.io.IOException;
import java.util.Arrays;

ListProjectsResponse listProjectsResponse = new ListProjectsResponse.Builder(
    Arrays.asList(
        new ListProject.Builder(
            1234567L,
            "returntocorp/semgrep",
            Arrays.asList(
                "tag"
            )
        )
        .createdAt("2020-11-18 23:28:12.391807+00:00")
        .defaultBranch("refs/heads/main")
        .latestScanAt("2023-01-13 20:51:51.449081+00:00")
        .primaryBranch("refs/heads/custom-main")
        .url("https://github.com/returntocorp/semgrep")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

