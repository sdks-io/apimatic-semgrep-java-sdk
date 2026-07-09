
# Protos Openapi V1 List Deployments Response

*This model accepts additional fields of type Object.*

## Structure

`ProtosOpenapiV1ListDeploymentsResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Deployments` | [`List<Deployment>`](../../doc/models/deployment.md) | Optional | Return the deployment the supplied token can access. | List<Deployment> getDeployments() | setDeployments(List<Deployment> deployments) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.Deployment;
import dev.semgrep.models.EndpointReference;
import dev.semgrep.models.ProtosOpenapiV1ListDeploymentsResponse;
import java.io.IOException;
import java.util.Arrays;

ProtosOpenapiV1ListDeploymentsResponse protosOpenapiV1ListDeploymentsResponse = new ProtosOpenapiV1ListDeploymentsResponse.Builder()
    .deployments(Arrays.asList(
        new Deployment.Builder(
            106L,
            "name6",
            "slug0"
        )
        .findings(new EndpointReference.Builder(
                "url2"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new Deployment.Builder(
            106L,
            "name6",
            "slug0"
        )
        .findings(new EndpointReference.Builder(
                "url2"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

