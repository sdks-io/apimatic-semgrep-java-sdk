
# Protos Openapi V1 Create Ticket Response Ticket Creation Success

*This model accepts additional fields of type Object.*

## Structure

`ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ExternalSlug` | `String` | Optional | The external slug identifier for the ticket | String getExternalSlug() | setExternalSlug(String externalSlug) |
| `IssueIds` | `List<Long>` | Optional | List of issue IDs | List<Long> getIssueIds() | setIssueIds(List<Long> issueIds) |
| `TicketId` | `Long` | Optional | The ID of the created ticket | Long getTicketId() | setTicketId(Long ticketId) |
| `TicketUrl` | `String` | Optional | The URL of the created ticket | String getTicketUrl() | setTicketUrl(String ticketUrl) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess;
import java.io.IOException;
import java.util.Arrays;

ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess protosOpenapiV1CreateTicketResponseTicketCreationSuccess = new ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess.Builder()
    .externalSlug("external_slug8")
    .issueIds(Arrays.asList(
        118L,
        117L
    ))
    .ticketId(114L)
    .ticketUrl("ticket_url6")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

