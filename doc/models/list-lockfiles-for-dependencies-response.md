
# List Lockfiles for Dependencies Response

*This model accepts additional fields of type Object.*

## Structure

`ListLockfilesForDependenciesResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Cursor` | `String` | Optional | Pass to next request to get next page of results. | String getCursor() | setCursor(String cursor) |
| `HasMore` | `boolean` | Required | True if there are more lockfiles to get. | boolean getHasMore() | setHasMore(boolean hasMore) |
| `LockfileSummaries` | [`List<ProtosScaV1LockfileDependencySummary>`](../../doc/models/protos-sca-v1-lockfile-dependency-summary.md) | Required | List of lockfiles. | List<ProtosScaV1LockfileDependencySummary> getLockfileSummaries() | setLockfileSummaries(List<ProtosScaV1LockfileDependencySummary> lockfileSummaries) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ListLockfilesForDependenciesResponse;
import dev.semgrep.models.ProtosScaV1LockfileDependencySummary;
import java.io.IOException;
import java.util.Arrays;

ListLockfilesForDependenciesResponse listLockfilesForDependenciesResponse = new ListLockfilesForDependenciesResponse.Builder(
    false,
    Arrays.asList(
        new ProtosScaV1LockfileDependencySummary.Builder()
            .lockfilePath("lockfilePath8")
            .numDependencies(0L)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    )
)
.cursor("cursor0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

