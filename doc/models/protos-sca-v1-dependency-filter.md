
# Protos Sca V1 Dependency Filter

Object to provide dependency details to filter by.

*This model accepts additional fields of type Object.*

## Structure

`ProtosScaV1DependencyFilter`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Ecosystem` | [`Ecosystem`](../../doc/models/ecosystem.md) | Optional | Filter by ecosystem (e.g. npm, pypi, etc).<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| no_package_manager \|  \|<br>\| npm \|  \|<br>\| pypi \|  \|<br>\| gomod \|  \|<br>\| cargo \|  \|<br>\| maven \|  \|<br>\| gem \|  \|<br>\| composer \|  \|<br>\| nuget \|  \|<br>\| pub \|  \|<br>\| swiftpm \|  \|<br>\| hex \|  \|<br>\| cocoapods \|  \|<br>\| mix \|  \|<br>\| opam \|  \| | Ecosystem getEcosystem() | setEcosystem(Ecosystem ecosystem) |
| `License` | `List<String>` | Optional | Filter by license (e.g. MIT). | List<String> getLicense() | setLicense(List<String> license) |
| `LicensePolicySettings` | [`LicensePolicySettings`](../../doc/models/license-policy-settings.md) | Optional | Filter by license policy setting outcome.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| LICENSE_POLICY_SETTING_ALLOW \|  \|<br>\| LICENSE_POLICY_SETTING_COMMENT \|  \|<br>\| LICENSE_POLICY_SETTING_BLOCK \|  \| | LicensePolicySettings getLicensePolicySettings() | setLicensePolicySettings(LicensePolicySettings licensePolicySettings) |
| `LockfilePath` | `String` | Optional | Filter by path to the lockfile (e.g. `foo/bar/package-lock.json`). | String getLockfilePath() | setLockfilePath(String lockfilePath) |
| `Name` | `String` | Optional | Deprecated - use package_filters instead. Filter by dependency name (e.g. lodash). | String getName() | setName(String name) |
| `PackageFilters` | [`List<ProtosScaV1PackageFilter>`](../../doc/models/protos-sca-v1-package-filter.md) | Optional | Multiple package filters with exact name matching and version bounds. | List<ProtosScaV1PackageFilter> getPackageFilters() | setPackageFilters(List<ProtosScaV1PackageFilter> packageFilters) |
| `RepositoryId` | `List<Long>` | Optional | Repository IDs (numeric) to filter by. Omit if the endpoint has Repository ID as a path parameter.<br>Use Projects endpoints to retrieve Repository IDs. | List<Long> getRepositoryId() | setRepositoryId(List<Long> repositoryId) |
| `Transitivity` | [`Transitivity`](../../doc/models/transitivity.md) | Optional | Filter by transitivity.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| UNKNOWN_TRANSITIVITY \|  \|<br>\| TRANSITIVE \|  \|<br>\| DIRECT \|  \| | Transitivity getTransitivity() | setTransitivity(Transitivity transitivity) |
| `Version` | `String` | Optional | Deprecated - use package_filters instead. Filter by dependency version (e.g. 1.0.1). | String getVersion() | setVersion(String version) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.Ecosystem;
import dev.semgrep.models.LicensePolicySettings;
import dev.semgrep.models.ProtosScaV1DependencyFilter;
import java.io.IOException;
import java.util.Arrays;

ProtosScaV1DependencyFilter protosScaV1DependencyFilter = new ProtosScaV1DependencyFilter.Builder()
    .ecosystem(Ecosystem.OPAM)
    .license(Arrays.asList(
        "license5"
    ))
    .licensePolicySettings(LicensePolicySettings.LICENSE_POLICY_SETTING_BLOCK)
    .lockfilePath("lockfilePath0")
    .name("name8")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

