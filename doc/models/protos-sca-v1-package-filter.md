
# Protos Sca V1 Package Filter

Individual package filter with optional version bounds.

*This model accepts additional fields of type Object.*

## Structure

`ProtosScaV1PackageFilter`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ExactNameMatch` | `Boolean` | Optional | When true, name must match exactly. When false (default), name is fuzzy-matched (contains). | Boolean getExactNameMatch() | setExactNameMatch(Boolean exactNameMatch) |
| `ExactVersion` | `String` | Optional | Exact version match (e.g. "1.0.0").<br>Takes precedence over version bounds if set. | String getExactVersion() | setExactVersion(String exactVersion) |
| `Name` | `String` | Optional | Exact package name (e.g. lodash). | String getName() | setName(String name) |
| `VersionLowerBound` | `String` | Optional | Lower bound version constraint (e.g. ">=1.0.0").<br>Ignored if exact_version is set. | String getVersionLowerBound() | setVersionLowerBound(String versionLowerBound) |
| `VersionUpperBound` | `String` | Optional | Upper bound version constraint (e.g. "<2.0.0").<br>Ignored if exact_version is set. | String getVersionUpperBound() | setVersionUpperBound(String versionUpperBound) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosScaV1PackageFilter;
import java.io.IOException;

ProtosScaV1PackageFilter protosScaV1PackageFilter = new ProtosScaV1PackageFilter.Builder()
    .exactNameMatch(false)
    .exactVersion("exactVersion4")
    .name("name6")
    .versionLowerBound("versionLowerBound8")
    .versionUpperBound("versionUpperBound8")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

