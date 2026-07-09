
# Deployment

Deployment record, with relevant meta-data and further accesses.

*This model accepts additional fields of type Object.*

## Structure

`Deployment`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Findings` | [`EndpointReference`](../../doc/models/endpoint-reference.md) | Optional | - | EndpointReference getFindings() | setFindings(EndpointReference findings) |
| `Id` | `long` | Required | Unique numerical identifier of the deployment. | long getId() | setId(long id) |
| `Name` | `String` | Required | Human readable name. | String getName() | setName(String name) |
| `Slug` | `String` | Required | Sanitized machine-readable name. Used as primary identifier through the web API. | String getSlug() | setSlug(String slug) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.Deployment;
import dev.semgrep.models.EndpointReference;
import java.io.IOException;

Deployment deployment = new Deployment.Builder(
    120L,
    "Your Deployment",
    "your-deployment"
)
.findings(new EndpointReference.Builder(
        "url2"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

