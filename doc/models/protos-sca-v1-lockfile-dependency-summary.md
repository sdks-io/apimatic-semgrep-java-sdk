
# Protos Sca V1 Lockfile Dependency Summary

*This model accepts additional fields of type Object.*

## Structure

`ProtosScaV1LockfileDependencySummary`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `LockfilePath` | `String` | Optional | Path to lockfile (e.g. foo/bar/package-lock.json). | String getLockfilePath() | setLockfilePath(String lockfilePath) |
| `NumDependencies` | `Long` | Optional | Total number of dependencies in the lockfile. | Long getNumDependencies() | setNumDependencies(Long numDependencies) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosScaV1LockfileDependencySummary;
import java.io.IOException;

ProtosScaV1LockfileDependencySummary protosScaV1LockfileDependencySummary = new ProtosScaV1LockfileDependencySummary.Builder()
    .lockfilePath("lockfilePath6")
    .numDependencies(152L)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

