
# Protos Scan V1 Scan Findings Counts

*This model accepts additional fields of type Object.*

## Structure

`ProtosScanV1ScanFindingsCounts`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Code` | `String` | Optional | Total number of Code findings in the scan | String getCode() | setCode(String code) |
| `Secrets` | `String` | Optional | Total number of Secrets findings in the scan | String getSecrets() | setSecrets(String secrets) |
| `SupplyChain` | `String` | Optional | Total number of Supply Chain findings in the scan | String getSupplyChain() | setSupplyChain(String supplyChain) |
| `Total` | `String` | Optional | Total number of findings in the scan | String getTotal() | setTotal(String total) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosScanV1ScanFindingsCounts;
import java.io.IOException;

ProtosScanV1ScanFindingsCounts protosScanV1ScanFindingsCounts = new ProtosScanV1ScanFindingsCounts.Builder()
    .code("2")
    .secrets("1")
    .supplyChain("1")
    .total("4")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

