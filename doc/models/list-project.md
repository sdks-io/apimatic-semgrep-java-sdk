
# List Project

A project in your organization that uses Semgrep.

*This model accepts additional fields of type Object.*

## Structure

`ListProject`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CreatedAt` | `String` | Optional | Time when this project was created. | String getCreatedAt() | setCreatedAt(String createdAt) |
| `DefaultBranch` | `String` | Optional | The default branch in the SCM. | String getDefaultBranch() | setDefaultBranch(String defaultBranch) |
| `Id` | `long` | Required | Unique ID of this project. | long getId() | setId(long id) |
| `LatestScanAt` | `String` | Optional | Time of latest scan, if there is one. | String getLatestScanAt() | setLatestScanAt(String latestScanAt) |
| `Name` | `String` | Required | Name of the project. | String getName() | setName(String name) |
| `PrimaryBranch` | `String` | Optional | The primary branch of the project, if known. | String getPrimaryBranch() | setPrimaryBranch(String primaryBranch) |
| `Tags` | `List<String>` | Required | Tags associated to this project. | List<String> getTags() | setTags(List<String> tags) |
| `Url` | `String` | Optional | URL of the project, if there is one. | String getUrl() | setUrl(String url) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ListProject;
import java.io.IOException;
import java.util.Arrays;

ListProject listProject = new ListProject.Builder(
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
.build();
```

