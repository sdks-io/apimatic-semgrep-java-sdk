
# Managed Scan Config

[Beta] Configuration of Semgrep Managed Scans for the project, if relevant.

*This model accepts additional fields of type Object.*

## Structure

`ManagedScanConfig`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DiffScan` | [`ProtosOpenapiV1DiffScan`](../../doc/models/protos-openapi-v1-diff-scan.md) | Optional | - | ProtosOpenapiV1DiffScan getDiffScan() | setDiffScan(ProtosOpenapiV1DiffScan diffScan) |
| `FullScan` | [`ProtosOpenapiV1FullScan`](../../doc/models/protos-openapi-v1-full-scan.md) | Optional | - | ProtosOpenapiV1FullScan getFullScan() | setFullScan(ProtosOpenapiV1FullScan fullScan) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ManagedScanConfig;
import dev.semgrep.models.ProtosOpenapiV1DiffScan;
import dev.semgrep.models.ProtosOpenapiV1FullScan;
import java.io.IOException;

ManagedScanConfig managedScanConfig = new ManagedScanConfig.Builder()
    .diffScan(new ProtosOpenapiV1DiffScan.Builder()
        .enabled(false)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .fullScan(new ProtosOpenapiV1FullScan.Builder()
        .enabled(false)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

