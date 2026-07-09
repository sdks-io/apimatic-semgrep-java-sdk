
# Endpoint Reference

*This model accepts additional fields of type Object.*

## Structure

`EndpointReference`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Url` | `String` | Required | URL that the reference is pointing to. | String getUrl() | setUrl(String url) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.EndpointReference;
import java.io.IOException;

EndpointReference endpointReference = new EndpointReference.Builder(
    "https://semgrep.dev/api/v1/deployments/123/findings"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

