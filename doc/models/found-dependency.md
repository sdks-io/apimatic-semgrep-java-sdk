
# Found Dependency

Information about the vulnerable package that was found in the codebase

*This model accepts additional fields of type Object.*

## Structure

`FoundDependency`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Ecosystem` | [`Ecosystem2`](../../doc/models/ecosystem-2.md) | Optional | Ecosystem of the package<br><br>**Default**: `Ecosystem2.NO_PACKAGE_MANAGER` | Ecosystem2 getEcosystem() | setEcosystem(Ecosystem2 ecosystem) |
| `LockfileLineUrl` | `String` | Optional | URL to the specific line in the lockfile where the dependency is listed | String getLockfileLineUrl() | setLockfileLineUrl(String lockfileLineUrl) |
| `Package` | `String` | Optional | Name of the package that contains the vulnerability | String getPackage() | setPackage(String mPackage) |
| `Transitivity` | [`Transitivity2`](../../doc/models/transitivity-2.md) | Optional | Indicates whether the dependency is direct or transitive | Transitivity2 getTransitivity() | setTransitivity(Transitivity2 transitivity) |
| `Version` | `String` | Optional | Version of the package that was found to be vulnerable | String getVersion() | setVersion(String version) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.Ecosystem2;
import dev.semgrep.models.FoundDependency;
import dev.semgrep.models.Transitivity2;
import java.io.IOException;

FoundDependency foundDependency = new FoundDependency.Builder()
    .ecosystem(Ecosystem2.NPM)
    .lockfileLineUrl("https://github.com/yourorg/yourrepo/blob/main/package-lock.json#L25")
    .mPackage("System.Drawing.Common")
    .transitivity(Transitivity2.DIRECT)
    .version("5.0.0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

