
# Protos Sca V1 Dependency

A specific dependency.

*This model accepts additional fields of type Object.*

## Structure

`ProtosScaV1Dependency`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | String identifier of dependency | String getName() | setName(String name) |
| `VersionSpecifier` | `String` | Optional | Version specifier of dependency. | String getVersionSpecifier() | setVersionSpecifier(String versionSpecifier) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosScaV1Dependency;
import java.io.IOException;

ProtosScaV1Dependency protosScaV1Dependency = new ProtosScaV1Dependency.Builder()
    .name("name2")
    .versionSpecifier("versionSpecifier0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

