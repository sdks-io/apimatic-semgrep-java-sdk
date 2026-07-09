
# List Repositories for Dependencies Response

*This model accepts additional fields of type Object.*

## Structure

`ListRepositoriesForDependenciesResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Cursor` | `Long` | Optional | Pass to next request to get next page of results. | Long getCursor() | setCursor(Long cursor) |
| `HasMore` | `boolean` | Required | True if there are more repositories to get. | boolean getHasMore() | setHasMore(boolean hasMore) |
| `RepositorySummaries` | [`List<ProtosScaV1RepositoryDependencySummary>`](../../doc/models/protos-sca-v1-repository-dependency-summary.md) | Required | List of repositories. | List<ProtosScaV1RepositoryDependencySummary> getRepositorySummaries() | setRepositorySummaries(List<ProtosScaV1RepositoryDependencySummary> repositorySummaries) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ListRepositoriesForDependenciesResponse;
import dev.semgrep.models.ProtosScaV1RepositoryDependencySummary;
import java.io.IOException;
import java.util.Arrays;

ListRepositoriesForDependenciesResponse listRepositoriesForDependenciesResponse = new ListRepositoriesForDependenciesResponse.Builder(
    false,
    Arrays.asList(
        new ProtosScaV1RepositoryDependencySummary.Builder()
            .hasDependencyPathScan(false)
            .id(140L)
            .name("name0")
            .numDependencies(226L)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    )
)
.cursor(48L)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

