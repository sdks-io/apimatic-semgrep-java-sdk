
# Protos Openapi V1 Diff Scan

*This model accepts additional fields of type Object.*

## Structure

`ProtosOpenapiV1DiffScan`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Enabled` | `Boolean` | Optional | When true, diff-aware scans are enabled for the project. | Boolean getEnabled() | setEnabled(Boolean enabled) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosOpenapiV1DiffScan;
import java.io.IOException;

ProtosOpenapiV1DiffScan protosOpenapiV1DiffScan = new ProtosOpenapiV1DiffScan.Builder()
    .enabled(false)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

