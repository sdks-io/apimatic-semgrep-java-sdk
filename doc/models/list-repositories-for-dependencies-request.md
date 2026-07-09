
# List Repositories for Dependencies Request

*This model accepts additional fields of type Object.*

## Structure

`ListRepositoriesForDependenciesRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Cursor` | `Long` | Optional | Use cursor in response to get next page of results. | Long getCursor() | setCursor(Long cursor) |
| `DependencyFilter` | [`ProtosScaV1DependencyFilter`](../../doc/models/protos-sca-v1-dependency-filter.md) | Optional | Object to provide dependency details to filter by. | ProtosScaV1DependencyFilter getDependencyFilter() | setDependencyFilter(ProtosScaV1DependencyFilter dependencyFilter) |
| `DeploymentId` | `String` | Required | Deployment ID (numeric). Example: `123`. Can be found at `/deployments`, or in your Settings in the web UI. | String getDeploymentId() | setDeploymentId(String deploymentId) |
| `PageSize` | `Long` | Optional | Number of repositories per page. Default: 5, min: 1, max: 100.<br><br>**Default**: `5L`<br><br>**Constraints**: `>= 1`, `<= 100` | Long getPageSize() | setPageSize(Long pageSize) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.Ecosystem;
import dev.semgrep.models.LicensePolicySettings;
import dev.semgrep.models.ListRepositoriesForDependenciesRequest;
import dev.semgrep.models.ProtosScaV1DependencyFilter;
import java.io.IOException;
import java.util.Arrays;

ListRepositoriesForDependenciesRequest listRepositoriesForDependenciesRequest = new ListRepositoriesForDependenciesRequest.Builder(
    "deploymentId2"
)
.cursor(236L)
.dependencyFilter(new ProtosScaV1DependencyFilter.Builder()
        .ecosystem(Ecosystem.MIX)
        .license(Arrays.asList(
            "license1",
            "license2"
        ))
        .licensePolicySettings(LicensePolicySettings.LICENSE_POLICY_SETTING_BLOCK)
        .lockfilePath("lockfilePath6")
        .name("name2")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.pageSize(100L)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

