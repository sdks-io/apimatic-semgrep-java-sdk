
# Bulk Triage Response

*This model accepts additional fields of type Object.*

## Structure

`BulkTriageResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NumTriaged` | `long` | Required | Number of items updated | long getNumTriaged() | setNumTriaged(long numTriaged) |
| `TriagedIssues` | `List<Long>` | Required | List of triaged issue IDs | List<Long> getTriagedIssues() | setTriagedIssues(List<Long> triagedIssues) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.BulkTriageResponse;
import java.io.IOException;
import java.util.Arrays;

BulkTriageResponse bulkTriageResponse = new BulkTriageResponse.Builder(
    232L,
    Arrays.asList(
        68L,
        69L,
        70L
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```

