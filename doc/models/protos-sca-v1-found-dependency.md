
# Protos Sca V1 Found Dependency

*This model accepts additional fields of type Object.*

## Structure

`ProtosScaV1FoundDependency`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DefinedAt` | [`ProtosScaV1CodeLocation`](../../doc/models/protos-sca-v1-code-location.md) | Optional | Path and line number dependency is declared in. | ProtosScaV1CodeLocation getDefinedAt() | setDefinedAt(ProtosScaV1CodeLocation definedAt) |
| `Ecosystem` | [`Ecosystem1`](../../doc/models/ecosystem-1.md) | Optional | The ecosystem the dependency is in (e.g. pypi, npm, etc).<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| no_package_manager \|  \|<br>\| npm \|  \|<br>\| pypi \|  \|<br>\| gomod \|  \|<br>\| cargo \|  \|<br>\| maven \|  \|<br>\| gem \|  \|<br>\| composer \|  \|<br>\| nuget \|  \|<br>\| pub \|  \|<br>\| swiftpm \|  \|<br>\| hex \|  \|<br>\| cocoapods \|  \|<br>\| mix \|  \|<br>\| opam \|  \| | Ecosystem1 getEcosystem() | setEcosystem(Ecosystem1 ecosystem) |
| `Licenses` | `List<String>` | Optional | Licenses the dependency is using. | List<String> getLicenses() | setLicenses(List<String> licenses) |
| `ManifestDefinition` | [`ProtosScaV1CodeLocation`](../../doc/models/protos-sca-v1-code-location.md) | Optional | Path to the manifest file that defines the subproject containing this dependency | ProtosScaV1CodeLocation getManifestDefinition() | setManifestDefinition(ProtosScaV1CodeLocation manifestDefinition) |
| `Package` | [`ProtosScaV1Dependency`](../../doc/models/protos-sca-v1-dependency.md) | Optional | What the dependency is. | ProtosScaV1Dependency getPackage() | setPackage(ProtosScaV1Dependency mPackage) |
| `RepositoryId` | `String` | Optional | ID of repository dependency is found in. | String getRepositoryId() | setRepositoryId(String repositoryId) |
| `ResolvedUrl` | `String` | Optional | The resolved URL of the dependency. Could point to a compressed source code directory (e.g. tarball), source code repository, or a package manager cache directory. May be empty if the package manager doesn't supply a URL. | String getResolvedUrl() | setResolvedUrl(String resolvedUrl) |
| `Transitivity` | [`Transitivity1`](../../doc/models/transitivity-1.md) | Optional | Whether dependency is direct or transitive.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| UNKNOWN_TRANSITIVITY \|  \|<br>\| TRANSITIVE \|  \|<br>\| DIRECT \|  \| | Transitivity1 getTransitivity() | setTransitivity(Transitivity1 transitivity) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.DateTimeHelper;
import dev.semgrep.models.Ecosystem1;
import dev.semgrep.models.ProtosScaV1CodeLocation;
import dev.semgrep.models.ProtosScaV1Dependency;
import dev.semgrep.models.ProtosScaV1FoundDependency;
import java.io.IOException;
import java.util.Arrays;

ProtosScaV1FoundDependency protosScaV1FoundDependency = new ProtosScaV1FoundDependency.Builder()
    .definedAt(new ProtosScaV1CodeLocation.Builder()
        .committedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .endCol("endCol8")
        .endLine("endLine2")
        .path("path2")
        .startCol("startCol2")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .ecosystem(Ecosystem1.GEM)
    .licenses(Arrays.asList(
        "licenses5",
        "licenses6",
        "licenses7"
    ))
    .manifestDefinition(new ProtosScaV1CodeLocation.Builder()
        .committedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .endCol("endCol0")
        .endLine("endLine4")
        .path("path4")
        .startCol("startCol4")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .mPackage(new ProtosScaV1Dependency.Builder()
        .name("name8")
        .versionSpecifier("versionSpecifier6")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

