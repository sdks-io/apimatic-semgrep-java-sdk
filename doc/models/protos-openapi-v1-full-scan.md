
# Protos Openapi V1 Full Scan

*This model accepts additional fields of type Object.*

## Structure

`ProtosOpenapiV1FullScan`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Enabled` | `Boolean` | Optional | When true, weekly full scans are enabled. | Boolean getEnabled() | setEnabled(Boolean enabled) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosOpenapiV1FullScan;
import java.io.IOException;

ProtosOpenapiV1FullScan protosOpenapiV1FullScan = new ProtosOpenapiV1FullScan.Builder()
    .enabled(false)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

