
# Protos Openapi V1 Search Scans Response

*This model accepts additional fields of type Object.*

## Structure

`ProtosOpenapiV1SearchScansResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Cursor` | `String` | Optional | Cursor to retrieve the next page of results. | String getCursor() | setCursor(String cursor) |
| `Scans` | [`List<ProtosScanV1ScanPublic>`](../../doc/models/protos-scan-v1-scan-public.md) | Optional | List of scans. | List<ProtosScanV1ScanPublic> getScans() | setScans(List<ProtosScanV1ScanPublic> scans) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.DateTimeHelper;
import dev.semgrep.models.ProtosOpenapiV1SearchScansResponse;
import dev.semgrep.models.ProtosScanV1ScanPublic;
import java.io.IOException;
import java.util.Arrays;

ProtosOpenapiV1SearchScansResponse protosOpenapiV1SearchScansResponse = new ProtosOpenapiV1SearchScansResponse.Builder()
    .cursor("cursor8")
    .scans(Arrays.asList(
        new ProtosScanV1ScanPublic.Builder()
            .branch("branch6")
            .commit("commit2")
            .completedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .deploymentId("deployment_id4")
            .enabledProducts(Arrays.asList(
                "enabled_products6",
                "enabled_products7"
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new ProtosScanV1ScanPublic.Builder()
            .branch("branch6")
            .commit("commit2")
            .completedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .deploymentId("deployment_id4")
            .enabledProducts(Arrays.asList(
                "enabled_products6",
                "enabled_products7"
            ))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

