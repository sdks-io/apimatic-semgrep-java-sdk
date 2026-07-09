
# Protos Sca V1 Repository Dependency Summary

*This model accepts additional fields of type Object.*

## Structure

`ProtosScaV1RepositoryDependencySummary`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `HasDependencyPathScan` | `Boolean` | Optional | True if the repository has been scanned with the `hasPathToTransitivityInScans` feature flag<br>which means it will have dependency graph data in DGraph available to query | Boolean getHasDependencyPathScan() | setHasDependencyPathScan(Boolean hasDependencyPathScan) |
| `Id` | `Long` | Optional | ID of repository. | Long getId() | setId(Long id) |
| `Name` | `String` | Optional | Name of repository. | String getName() | setName(String name) |
| `NumDependencies` | `Long` | Optional | Total number of dependencies in the repository. | Long getNumDependencies() | setNumDependencies(Long numDependencies) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosScaV1RepositoryDependencySummary;
import java.io.IOException;

ProtosScaV1RepositoryDependencySummary protosScaV1RepositoryDependencySummary = new ProtosScaV1RepositoryDependencySummary.Builder()
    .hasDependencyPathScan(false)
    .id(78L)
    .name("name4")
    .numDependencies(164L)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

