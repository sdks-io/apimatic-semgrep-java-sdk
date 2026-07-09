
# Protos Openapi V1 Unlink Ticket Response

*This model accepts additional fields of type Object.*

## Structure

`ProtosOpenapiV1UnlinkTicketResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `UnlinkedIssueIds` | `List<String>` | Optional | List of finding IDs that were successfully unlinked from their tickets | List<String> getUnlinkedIssueIds() | setUnlinkedIssueIds(List<String> unlinkedIssueIds) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosOpenapiV1UnlinkTicketResponse;
import java.io.IOException;
import java.util.Arrays;

ProtosOpenapiV1UnlinkTicketResponse protosOpenapiV1UnlinkTicketResponse = new ProtosOpenapiV1UnlinkTicketResponse.Builder()
    .unlinkedIssueIds(Arrays.asList(
        "unlinked_issue_ids6",
        "unlinked_issue_ids7",
        "unlinked_issue_ids8"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

