
# Protos Openapi V1 Create Ticket Response Ticket Creation Skipped

*This model accepts additional fields of type Object.*

## Structure

`ProtosOpenapiV1CreateTicketResponseTicketCreationSkipped`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `IssueIds` | `List<Long>` | Optional | List of issue IDs | List<Long> getIssueIds() | setIssueIds(List<Long> issueIds) |
| `Reason` | `String` | Optional | The reason why the issue was skipped | String getReason() | setReason(String reason) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosOpenapiV1CreateTicketResponseTicketCreationSkipped;
import java.io.IOException;
import java.util.Arrays;

ProtosOpenapiV1CreateTicketResponseTicketCreationSkipped protosOpenapiV1CreateTicketResponseTicketCreationSkipped = new ProtosOpenapiV1CreateTicketResponseTicketCreationSkipped.Builder()
    .issueIds(Arrays.asList(
        74L,
        75L
    ))
    .reason("reason4")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

