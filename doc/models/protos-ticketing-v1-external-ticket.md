
# Protos Ticketing V1 External Ticket

*This model accepts additional fields of type Object.*

## Structure

`ProtosTicketingV1ExternalTicket`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ExternalSlug` | `String` | Optional | Identifier of the external ticket (e.g. for Jira, something like OPS-158). | String getExternalSlug() | setExternalSlug(String externalSlug) |
| `Id` | `String` | Optional | Nango ticket id | String getId() | setId(String id) |
| `LinkedIssueIds` | `List<String>` | Optional | Semgrep issue ids that are linked to this external ticket | List<String> getLinkedIssueIds() | setLinkedIssueIds(List<String> linkedIssueIds) |
| `Url` | `String` | Optional | URL of the external ticket. | String getUrl() | setUrl(String url) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ProtosTicketingV1ExternalTicket;
import java.io.IOException;
import java.util.Arrays;

ProtosTicketingV1ExternalTicket protosTicketingV1ExternalTicket = new ProtosTicketingV1ExternalTicket.Builder()
    .externalSlug("externalSlug6")
    .id("id6")
    .linkedIssueIds(Arrays.asList(
        "linkedIssueIds7"
    ))
    .url("url0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

