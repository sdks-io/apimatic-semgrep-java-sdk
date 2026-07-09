
# Protos Openapi V1 Link Ticket Response

*This model accepts additional fields of type Object.*

## Structure

`ProtosOpenapiV1LinkTicketResponse`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ExternalSlug` | `String` | Optional | The external slug identifier for the ticket (e.g. SEC-123) | String getExternalSlug() | setExternalSlug(String externalSlug) |
| `LinkedIssueIds` | `List<String>` | Optional | List of finding IDs that were successfully linked to the ticket | List<String> getLinkedIssueIds() | setLinkedIssueIds(List<String> linkedIssueIds) |
| `ReplacedIssueIds` | `List<String>` | Optional | List of finding IDs where an existing ticket link was replaced | List<String> getReplacedIssueIds() | setReplacedIssueIds(List<String> replacedIssueIds) |
| `TicketId` | `Long` | Optional | The internal ID of the linked ticket record | Long getTicketId() | setTicketId(Long ticketId) |
| `TicketUrl` | `String` | Optional | The URL of the linked ticket | String getTicketUrl() | setTicketUrl(String ticketUrl) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosOpenapiV1LinkTicketResponse;
import java.io.IOException;
import java.util.Arrays;

ProtosOpenapiV1LinkTicketResponse protosOpenapiV1LinkTicketResponse = new ProtosOpenapiV1LinkTicketResponse.Builder()
    .externalSlug("external_slug4")
    .linkedIssueIds(Arrays.asList(
        "linked_issue_ids1"
    ))
    .replacedIssueIds(Arrays.asList(
        "replaced_issue_ids5"
    ))
    .ticketId(148L)
    .ticketUrl("ticket_url8")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

