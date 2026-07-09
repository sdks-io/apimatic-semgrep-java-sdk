
# Create Sbom Export Response

*This model accepts additional fields of type Object.*

## Structure

`CreateSbomExportResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TaskToken` | `String` | Required | Task token for the SBOM export job. | String getTaskToken() | setTaskToken(String taskToken) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.CreateSbomExportResponse;
import java.io.IOException;

CreateSbomExportResponse createSbomExportResponse = new CreateSbomExportResponse.Builder(
    "taskToken6"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

