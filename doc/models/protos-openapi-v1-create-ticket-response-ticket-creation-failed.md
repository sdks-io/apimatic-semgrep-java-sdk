
# Protos Openapi V1 Create Ticket Response Ticket Creation Failed

*This model accepts additional fields of type Object.*

## Structure

`ProtosOpenapiV1CreateTicketResponseTicketCreationFailed`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Error` | `String` | Optional | The error message for the failure | String getError() | setError(String error) |
| `IssueIds` | `List<Long>` | Optional | List of issue IDs | List<Long> getIssueIds() | setIssueIds(List<Long> issueIds) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosOpenapiV1CreateTicketResponseTicketCreationFailed;
import java.io.IOException;
import java.util.Arrays;

ProtosOpenapiV1CreateTicketResponseTicketCreationFailed protosOpenapiV1CreateTicketResponseTicketCreationFailed = new ProtosOpenapiV1CreateTicketResponseTicketCreationFailed.Builder()
    .error("error8")
    .issueIds(Arrays.asList(
        36L,
        37L
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

