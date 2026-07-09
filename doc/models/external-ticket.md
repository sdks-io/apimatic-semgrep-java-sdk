
# External Ticket

External ticket associated with finding

*This model accepts additional fields of type Object.*

## Structure

`ExternalTicket`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ExternalSlug` | `String` | Optional | Identifier of the external ticket | String getExternalSlug() | setExternalSlug(String externalSlug) |
| `Id` | `Long` | Optional | External ticket id | Long getId() | setId(Long id) |
| `LinkedIssueIds` | `List<Long>` | Optional | Semgrep issue ids that are linked to this external ticket | List<Long> getLinkedIssueIds() | setLinkedIssueIds(List<Long> linkedIssueIds) |
| `Url` | `String` | Optional | URL of the external ticket | String getUrl() | setUrl(String url) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |

## Example

```java
import dev.semgrep.ApiHelper;
import dev.semgrep.models.ExternalTicket;
import java.io.IOException;
import java.util.Arrays;

ExternalTicket externalTicket = new ExternalTicket.Builder()
    .externalSlug("OPS-158")
    .id(74L)
    .linkedIssueIds(Arrays.asList(
        217L,
        218L
    ))
    .url("url0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```

