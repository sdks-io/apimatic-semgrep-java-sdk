
# List Dependencies Request

*This model accepts additional fields of type Object.*

## Structure

`ListDependenciesRequest`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Cursor` | `String` | Optional | Cursor to paginate through the dependencies. Provide a cursor value from the response to retrieve the next page. | String getCursor() | setCursor(String cursor) |
| `DependencyFilter` | [`ProtosScaV1DependencyFilter`](../../doc/models/protos-sca-v1-dependency-filter.md) | Optional | Object to provide dependency details to filter by. | ProtosScaV1DependencyFilter getDependencyFilter() | setDependencyFilter(ProtosScaV1DependencyFilter dependencyFilter) |
| `DeploymentId` | `String` | Required | Deployment ID (numeric). Example: `123`. Can be found at `/deployments`, or in your Settings in the web UI. | String getDeploymentId() | setDeploymentId(String deploymentId) |
| `PageSize` | `Long` | Optional | Number of dependencies per page. Default: 1000, min: 1, max: 10000.<br><br>**Constraints**: `>= 1`, `<= 10000` | Long getPageSize() | setPageSize(Long pageSize) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.Ecosystem;
import dev.semgrep.models.LicensePolicySettings;
import dev.semgrep.models.ListDependenciesRequest;
import dev.semgrep.models.ProtosScaV1DependencyFilter;
import java.io.IOException;
import java.util.Arrays;

ListDependenciesRequest listDependenciesRequest = new ListDependenciesRequest.Builder(
    "123"
)
.cursor("cursor2")
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
.pageSize(1000L)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

